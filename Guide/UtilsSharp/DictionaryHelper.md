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
static Dictionary<string, string> ObjToDictionaryStringValue(object obj)
```

#### 2、 转换对象为字典：ObjToDictionary
```c#
/// <summary>
/// 转换对象为字典
/// </summary>
/// <param name="obj">要转换的对象</param>
/// <returns>返回字典</returns>
static Dictionary<string, object> ObjToDictionary(object obj)
```
```c#
/// <summary>
/// 转换对象为字典
/// </summary>
/// <param name="obj">要转换的对象</param>
/// <param name="members">需要转换的成员</param>
/// <param name="ignoreMembers">忽略转换的成员</param>
/// <returns>返回字典</returns>
static Dictionary<string, object> ObjToDictionary(object obj, string[] members, string[] ignoreMembers)
```
#### 3、转换字典为对象：DictionaryToObj
```c#
/// <summary>
/// 转换字典为对象
/// </summary>
/// <param name="dictionary">要转换的字典</param>
/// <returns>返回对象</returns>
static T DictionaryToObj<T>(Dictionary<string, object> dictionary) where T : class, new()
```
```c#
/// <summary>
/// 转换字典为对象
/// </summary>
/// <param name="dictionary">要转换的字典</param>
/// <param name="members">需要转换的成员</param>
/// <param name="ignoreMembers">忽略转换的成员</param>
/// <returns>返回对象</returns>
static T DictionaryToObj<T>(Dictionary<string, object> dictionary, string[] members, string[] ignoreMembers)where T:class,new()
```

