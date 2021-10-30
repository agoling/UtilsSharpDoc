# UtilsSharp帮助类：DictionaryHelper

`DictionaryHelper`字典帮助类帮助类共有以下几个方法

本类方法是静态方法无需实例化后使用，使用方法：

```c#
DictionaryHelper.ObjToDictionaryStringValue("{\"abc\":\"abc\"}")
```

#### 1、转换对象为字典：ObjToDictionaryStringValue

```c#
/// <summary>
/// 转换对象为字典
/// </summary>
/// <param name="obj">要转换的对象</param>
/// <returns>返回字典</returns>
static Dictionary<string, string> ToDictionaryStringValue(this object obj)
```

#### 2、 转换对象为字典：ObjToDictionary
```c#
/// <summary>
/// 转换对象为字典
/// </summary>
/// <param name="obj">要转换的对象</param>
/// <returns>返回字典</returns>
static Dictionary<string, object> ToDictionary(this object obj)
```
```c#
/// <summary>
/// 转换对象为字典
/// </summary>
/// <param name="obj">要转换的对象</param>
/// <param name="members">需要转换的成员</param>
/// <param name="ignoreMembers">忽略转换的成员</param>
/// <returns>返回字典</returns>
static Dictionary<string, object> ToDictionary(this object obj, string[] members, string[] ignoreMembers)
```
#### 3、转换字典为对象：DictionaryToObj
```c#
/// <summary>
/// 转换字典为对象
/// </summary>
/// <param name="dictionary">要转换的字典</param>
/// <returns>返回对象</returns>
static T ToEntity<T>(this Dictionary<string, object> dictionary) where T : class, new()
```
```c#
/// <summary>
/// 转换字典为对象
/// </summary>
/// <param name="dictionary">要转换的字典</param>
/// <param name="members">需要转换的成员</param>
/// <param name="ignoreMembers">忽略转换的成员</param>
/// <returns>返回对象</returns>
static T ToEntity<T>(this Dictionary<string, object> dictionary, string[] members, string[] ignoreMembers)where T:class,new()
```

#### 4、获取字典值：GetValue

```c#
/// <summary>
/// 获取字典值
/// </summary>
/// <param name="dic">字典</param>
/// <param name="key">字典Key</param>
/// <returns></returns>
static string GetValue(this Dictionary<string, string> dic, string key)
```

```c#
/// <summary>
/// 获取字典值
/// </summary>
/// <typeparam name="T">类型</typeparam>
/// <param name="dic">字典</param>
/// <param name="key">字典Key</param>
/// <returns></returns>
static T GetValue<T>(this Dictionary<string, object> dic, string key)
```

#### 5、字典转Dynamic：ToDynamic

```c#
/// <summary>
/// 字典转Dynamic
/// </summary>
/// <param name="dic">字典</param>
/// <returns></returns>
static dynamic ToDynamic(this Dictionary<string, object> dic)
```

