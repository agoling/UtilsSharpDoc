# UtilsSharp帮助类：IpHelper
`IpHelper`Ip帮助类,包括获取客户端和服务端Ip方法，以及获取Ip信息

本类方法是静态方法无需实例化，可直接使用。

#### 1、获取客户端Ip：GetClientIp

```c#
/// <summary>
/// 获取客户端Ip
/// </summary>
/// <returns></returns>
static string GetClientIp()
```

#### 2、获取服务端Ip：GetServerIp

```c#
/// <summary>
/// 获取服务端Ip
/// </summary>
/// <returns></returns>
static string GetServerIp()
```

#### 3、获取Ip详细信息：GetIpInfo

```c#
/// <summary>
/// 获取Ip详细信息
/// </summary>
/// <param name="ip">ip</param>
/// <returns></returns>
static IpInfo GetIpInfo(string ip)
```

