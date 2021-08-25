# UtilsSharp帮助类：CacheHelper
`CacheHelper`服务器缓存帮助类实现`UtilsSharp.Standard.Interface.ICacheManager`接口，共有以下几个方法

本类需要实例化后使用，使用方法：

```c#
CacheHelper cacheHelper=new CacheHelper(); 
```

#### 1、获取当前缓存类型：GetCacheTypeName

因为`ICacheManager`接口有可能被多个缓存类型实现，比如`Redis`、`MemCache`等，这个方法主要就是返回当前类是什么类型的缓存，本类返回的是服务器机器缓存，所以返回值是`MemoryCache`。

```c#
/// <summary>
/// 获取当前缓存实例类型名字
/// </summary>
/// <returns></returns>
string GetCacheTypeName()
```

#### 2、添加缓存：Set

添加缓存共有两个重载

```c#
/// <summary>
/// 添加缓存
/// </summary>
/// <param name="key">缓存key</param>
/// <param name="value">缓存数据</param>
/// <param name="expireSeconds">缓存时间(秒)</param>
/// <returns>是否成功</returns>
bool Set(string key, object value, int expireSeconds = -1)
```

```c#
/// <summary>
/// 添加缓存
/// </summary>
/// <param name="key">缓存key</param>
/// <param name="value">缓存数据</param>
/// <param name="expire">缓存时间戳</param>
/// <returns>是否成功</returns>
bool Set(string key, object value, TimeSpan expire)
```

#### 3、获取缓存：Get

获取缓存共有两个重载

```c#
/// <summary>
/// 获取缓存
/// </summary>
/// <param name="key">缓存Key</param>
/// <returns>缓存数据</returns>
string Get(string key)
```

```c#
/// <summary>
/// 获取缓存
/// </summary>
/// <typeparam name="T">缓存数据类型</typeparam>
/// <param name="key">缓存Key</param>
/// <returns>缓存数据</returns>
T Get<T>(string key)
```

#### 4、验证缓存是否存在：IsExists

```c#
/// <summary>
/// 验证缓存是否存在
/// </summary>
/// <param name="key">缓存key</param>
/// <returns >是否存在</returns>
bool IsExists(string key)
```

#### 5、移除缓存：Remove

```c#
/// <summary>
/// 移除缓存
/// </summary>
/// <param name="keys">缓存keys</param>
long Remove(params string[] keys)
```
