# UtilsSharp帮助类：WebHelper
`WebHelper`网络请求工具帮助类共有以下几个方法

本类是继承自WebClient类，需要实例化后使用，使用方法：

```c#
using (var webHelper = new WebHelper())
{
  var dic = new Dictionary<string, string> { { "sign", "b486a1fa5e024be0a45c096ca5f6cfec" } };
  var url = $"https://www.baidu.com/api/xxxxxx";
  webHelper.Headers.Add("Content-Type", "application/json;charset=UTF-8");//Header设置
  webHelper.Proxy=new WebProxy("127.0.0.1:98"){Credentials = new NetworkCredential("username","password")};//代理请求
  webHelper.Encoding = Encoding.UTF8;//编码
  webHelper.Timeout = 10;//请求超时时间 单位秒
  var requestResult = webHelper.DoPost(url, dic);
  var requestTResult = webHelper.DoPost<BaseResult<string>>(url, dic).HandleResult();
}
```

#### 1、Get请求：DoGet

```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
BaseResult<string> DoGet(string address, object parameters)
```

```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
async Task<BaseResult<string>> DoGetAsync(string address, object parameters)
```

```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
BaseResult<T> DoGet<T>(string address, object parameters) where T : class, new()
```
```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
async Task<BaseResult<T>> DoGetAsync<T>(string address, object parameters) where T : class, new()
```

```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <returns></returns>
BaseResult<string> DoGet(string address)
```
```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <returns></returns>
async Task<BaseResult<string>> DoGetAsync(string address)
```
```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <returns></returns>
BaseResult<T> DoGet<T>(string address) where T : class, new()
```
```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <returns></returns>
async Task<BaseResult<T>> DoGetAsync<T>(string address) where T : class, new()
```
```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
BaseResult<string> DoGet(string address, Dictionary<string, string> parameters)
```
```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
async Task<BaseResult<string>> DoGetAsync(string address, Dictionary<string, string> parameters)
```
```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
BaseResult<T> DoGet<T>(string address, Dictionary<string, string> parameters) where T : class, new()
```
```c#
/// <summary>
/// Get请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
async Task<BaseResult<T>> DoGetAsync<T>(string address, Dictionary<string, string> parameters) where T : class, new()
```
#### 2、Post请求：DoPost

```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <returns></returns>
BaseResult<string> DoPost(string address)
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <returns></returns>
async Task<BaseResult<string>> DoPostAsync(string address)
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <returns></returns>
BaseResult<T> DoPost<T>(string address) where T : class, new()
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <returns></returns>
async Task<BaseResult<T>> DoPostAsync<T>(string address) where T : class, new()
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
BaseResult<string> DoPost(string address, Dictionary<string, string> parameters)
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
async Task<BaseResult<string>> DoPostAsync(string address, Dictionary<string, string> parameters)
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
BaseResult<T> DoPost<T>(string address, Dictionary<string, string> parameters) where T : class, new()
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <returns></returns>
async Task<BaseResult<T>> DoPostAsync<T>(string address, Dictionary<string, string> parameters) where T : class, new()
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <param name="dateTimeFormat">返回的时间格式</param>
/// <returns></returns>
BaseResult<string> DoPost(string address, object parameters, string dateTimeFormat = "yyyy-MM-dd HH:mm:ss")
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <param name="dateTimeFormat">返回的时间格式</param>
/// <returns></returns>
async Task<BaseResult<string>> DoPostAsync(string address, object parameters,string dateTimeFormat = "yyyy-MM-dd HH:mm:ss")
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <param name="dateTimeFormat">返回的时间格式</param>
/// <returns></returns>
BaseResult<T> DoPost<T>(string address, object parameters, string dateTimeFormat = "yyyy-MM-dd HH:mm:ss") where T : class, new()
```
```c#
/// <summary>
/// Post请求
/// </summary>
/// <param name="address">请求地址</param>
/// <param name="parameters">请求参数</param>
/// <param name="dateTimeFormat">返回的时间格式</param>
/// <returns></returns>
async Task<BaseResult<T>> DoPostAsync<T>(string address, object parameters,string dateTimeFormat = "yyyy-MM-dd HH:mm:ss") where T : class, new()
```

