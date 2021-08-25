# UtilsSharp帮助类：AppsettingsHelper

`AppsettingsHelper`配置文件帮助类共有以下几个方法

ben本类方法是静态方法无需实例化后使用，使用方法：

在使用本类之前，如果项目下面无`appsettings.json`文件，则需要添加`appsettings.json`，并设置文件属性中的“复制到输出目录”为始终复制。

#### 1、根据key获取对应的配置值：GetValue

```c#
/// <summary>
/// 根据key获取对应的配置值
/// </summary>
/// <param name="key">key</param>
/// <returns></returns>
static string GetValue(string key)
```

#### 2、获取ConnectionStrings下默认的配置连接字符串：GetConnectionString

```c#
/// <summary>
/// 获取ConnectionStrings下默认的配置连接字符串
/// </summary>
/// <param name="key">key</param>
/// <returns></returns>
static string GetConnectionString(string key)
```

#### 3、根据key获取对应节点的配置值：GetSection

```c#
/// <summary>
/// 根据key获取对应节点的配置值
/// </summary>
/// <param name="key">key:子节点冒号隔开,如aa:bb</param>
/// <returns></returns>
static IConfigurationSection GetSection(string key)
```

```c#
/// <summary>
/// 根据key获取对应节点的配置值
/// </summary>
/// <param name="key">key:子节点冒号隔开,如aa:bb</param>
/// <returns></returns>
static T GetSection<T>(string key)
```

#### 4、获取所有配置子节点：GetChildren

```c#
/// <summary>
/// 获取所有配置子节点
/// </summary>
/// <returns></returns>
static IEnumerable<IConfigurationSection> GetChildren()
```

