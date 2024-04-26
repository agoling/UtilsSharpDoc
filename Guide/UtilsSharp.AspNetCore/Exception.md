

# Exception异常处理

Exception异常处理，主要分为两个部分，一种是aop全局拦截，另外一种是try  catch异常捕获。

##### 使用方法：

1、try catch 异常捕获：需要安装UtilsSharp工具类。注意：包版本要3.4及以上。

2、aop全局捕获：需要在控制器层安装UtilsSharp.AspNetCore工具类。注意：包版本要3.4及以上,只有方法中没有做try catch的异常才会被捕捉到

#### 一、try catch 异常捕获

##### 1、设置字符串

```c#
using UtilsSharp;

/// <summary>
/// 获取用户信息
/// </summary>
/// <param name="request">获取用户信息参数</param>
/// <returns></returns>
public BaseResult<GetUserInfoResponse> GetUserInfo(GetUserInfoRequest request)
{
   var result = new BaseResult<GetUserInfoResponse>();
   try
    {
      /*…这边省略业务代码…*/
      //假如抛出了异常
      throw new Exception("db error 异常错误");
    }
    catch (Exception ex)
    {
      /*第一种捕获异常信息方式
        该种会把用户填写的字符串赋值给result.Msg
      */
      result.SetException("异常");
      return result;
    }
}
```
第一种返回效果：
![](Image\20240426111800.jpg)

##### 2、设置Exception对象
```c#
using UtilsSharp;

/// <summary>
/// 获取用户信息
/// </summary>
/// <param name="request">获取用户信息参数</param>
/// <returns></returns>
public BaseResult<GetUserInfoResponse> GetUserInfo(GetUserInfoRequest request)
{
   var result = new BaseResult<GetUserInfoResponse>();
   try
    {
      /*…这边省略业务代码…*/
      //假如抛出了异常
      throw new Exception("db error 异常错误");
    }
    catch (Exception ex)
    {
      /*第二种捕获异常信息方式
        该种方式会去捕获ex.Message+ex.StackTrace里面的内容并赋值给result.Msg
      */
      result.SetException(ex);
      return result;
    }
}
```
第二种返回效果：
![](Image\20240426115738.jpg)

##### 3、设置Exception对象、日志Id、匹配规则
```c#
using UtilsSharp;

/// <summary>
/// 获取用户信息
/// </summary>
/// <param name="request">获取用户信息参数</param>
/// <returns></returns>
public BaseResult<GetUserInfoResponse> GetUserInfo(GetUserInfoRequest request)
{
   var result = new BaseResult<GetUserInfoResponse>();
   try
    {
      /*…这边省略业务代码…*/
      //假如抛出了异常
      throw new Exception("db error 异常错误");
    }
    catch (Exception ex)
    {
      /*第三种捕获异常信息方式
        1、该种方式会去匹配ex.Message+ex.StackTrace里面的内容，如果命中规则中指定的关键词，会把相应错误赋值给result.Msg
        2、比如该异常命中了db error这个词（不区分大小写）会有相应的code和msg拓传出来
      */
      var logId = LogHelperesult.Error($"异常", ex);//先把异常写入日志,返回日志Id(错误码)
      var rules = new List<ExceptionRegexRule>
      {
        new ExceptionRegexRule { Code = BaseStateCode.数据库异常, Rules = new List<string> { "db error","库异常","db异常" }}
      };
      result.SetException(ex, logId, rules);
      return result;
    }
}
```
第三种返回效果：
![](Image\20240426113806.jpg)

##### 4、设置Exception对象、日志Id、匹配规则、自定义提示信息
```c#
using UtilsSharp;

/// <summary>
/// 获取用户信息
/// </summary>
/// <param name="request">获取用户信息参数</param>
/// <returns></returns>
public BaseResult<GetUserInfoResponse> GetUserInfo(GetUserInfoRequest request)
{
   var result = new BaseResult<GetUserInfoResponse>();
   try
    {
      /*…这边省略业务代码…*/
      //假如抛出了异常
      throw new Exception("db error 异常错误");
    }
    catch (Exception ex)
    {
      /*第四种捕获异常信息方式
        1、这种跟第三种一样
        2、只是增加了自定义提示词Msg="亲，不好意思，数据库异常了"，所以msg提示词用自定义的
      */
      var logId = LogHelperesult.Error($"异常", ex);//先把异常写入日志,返回日志Id(错误码)
      var rules = new List<ExceptionRegexRule>
      {
        new ExceptionRegexRule { Code = BaseStateCode.数据库异常, Rules = new List<string> { "db error","数据库异常","db异常" },Msg="亲，不好意思，数据库异常了"}
      };
      result.SetException(ex, logId, rules);
      return result;
    }
}
```
第四种返回效果：
![](Image\20240426113256.jpg)

##### 5、设置Exception对象、日志Id（默认）
```c#
using UtilsSharp;

/// <summary>
/// 获取用户信息
/// </summary>
/// <param name="request">获取用户信息参数</param>
/// <returns></returns>
public BaseResult<GetUserInfoResponse> GetUserInfo(GetUserInfoRequest request)
{
   var result = new BaseResult<GetUserInfoResponse>();
   try
    {
      /*…这边省略业务代码…*/
      //假如抛出了未授权异常
      throw new Exception("Unauthorized 异常错误");
    }
    catch (Exception ex)
    {
      /*第五种捕获异常信息方式（推荐）
        1、这种跟三、四两种是一样的，只是默认了一些List<ExceptionRegexRule>的规则
        2、这边主要默认了两种规则，“授权过期”和“未登入”两种场景，如果命中它们的关键词，就会提示相应报错
        3、默认规则：
        var rules = new List<ExceptionRegexRule>
        {
          new ExceptionRegexRule { Code = BaseStateCode.授权过期, Rules = new List<string> { "unauthorized", "request need user authorized", "授权过期", "授权失效", "未授权" },Msg="" },
          new ExceptionRegexRule { Code = BaseStateCode.未登录, Rules = new List<string> { "未登入", "登入过期", "登入失效", "未登录", "登录过期", "登录失效", "token过期", "token expires" },Msg="" }
         };
      */
      var logId = LogHelperesult.Error($"异常", ex);//先把异常写入日志
      result.SetException(ex, logId);//得到的日志id,返回日志Id(错误码)
      return result;
    }
}
```
第五种返回效果：
![](Image\20240426112538.jpg)

#### 二、Aop全局捕获

##### 1、nuget直接安装UtilsSharp.AspNetCore框架(3.4以上版本)，在Startup.cs文件简单配置即可

```c#
    public class Startup : AutofacStartup
    {
        public Startup(IConfiguration configuration)
        {
            Configuration = configuration;
        }
 
        public IConfiguration Configuration { get; }
 
        // This method gets called by the runtime. Use this method to add services to the container.
        public void ConfigureServices(IServiceCollection services)
        {
            //初始化Protobuf模型
            //ProtobufRunTime.Initialize();
            // 验证入参模型
            //services.AddValidationExtensions();
            //ElasticSearch配置
            //ElasticSearchConfig.ElasticSearchSetting = JsonConvert.DeserializeObject<ElasticSearchSetting>(BaseConfig.EsSettingJson);
            //MQ队列配置
            //RabbitMqConfig.RabbitMqSetting = new RabbitMqSetting { RabbitMqConnection =BaseConfig.RabbitMqConnection};
            //RabbitMqManager.Register();
            //swagger配置
            //AspNetCoreExtensionsConfig.SwaggerDocOptions = new SwaggerDocOptions
            //{
            //    Enable = true,
            //    ProjectName = "日志管理中心",
            //    ProjectDescription = "日志管理中心接口",
            //    Groups = new List<SwaggerGroup>
            //    {
            //        new SwaggerGroup() {GroupName = "log", Title = "日志记录接口", Version = "v1.0"}
            //    }
            //};
            //ThreadPool.SetMinThreads(500, 400);
            services.AddAspNetCoreExtensions();
            services.AddControllers().AddNewtonsoftJson();
        }
 
        // This method gets called by the runtime. Use this method to configure the HTTP request pipeline.
        public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            if (env.IsDevelopment())
            {
                app.UseDeveloperExceptionPage();
            }
 
            //注册扩展
            app.UseAspNetCoreExtensions();
            app.UseRouting();
 
            app.UseEndpoints(endpoints =>
            {
                //配置控制器映射
                endpoints.MapControllers();
            });
        }
 
        /// <summary>
        /// 依赖注入映射
        /// </summary>
        /// <param name="builder"></param>
        public override void ConfigureContainer(ContainerBuilder builder)
        {
            Init<AsyncInterceptor<LoggerAsyncInterceptor>>(builder);
        }
    }
```
命中Unauthorized这个词的返回效果：
![](Image\20240426143450.jpg)

##### 2、如果要全局自定义拦截规则，则要重写LoggerAsyncInterceptor类
```c#
public class Startup : AutofacStartup
{
      /*以上代码省略*/
 
     /// <summary>
     /// 依赖注入映射
     /// </summary>
     /// <param name="builder"></param>
     public override void ConfigureContainer(ContainerBuilder builder)
     {
       Init<AsyncInterceptor<LoggerAsyncInterceptorNew>>(builder);
     }
}    

/// <summary>
/// 重写LoggerAsyncInterceptor
/// </summary>
public class LoggerAsyncInterceptorNew: LoggerAsyncInterceptor
{
    /// <summary>
    /// Exception 匹配规则
    /// </summary>
    public override List<ExceptionRegexRule> ExceptionRegexRule { set; get; } = new List<ExceptionRegexRule>
    {
      new ExceptionRegexRule { Code = BaseStateCode.授权过期, Rules = new List<string> { "unauthorized", "request need user authorized", "授权过期", "授权失效", "未授权" },Msg="" },
      new ExceptionRegexRule { Code = BaseStateCode.未登录, Rules = new List<string> { "未登入", "登入过期", "登入失效", "未登录", "登录过期", "登录失效", "token过期", "token expires" },Msg="" },
      new ExceptionRegexRule { Code = BaseStateCode.数据库异常, Rules = new List<string> { "db error"},Msg="老板对不起，数据库错误了" }
    };
}
```
命中db error这个词的返回效果：
![](Image\20240426143229.jpg)

