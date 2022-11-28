# UtilsSharp帮助类：JsonHelper

`JsonHelper`Json帮助类

本类是静态类无需实例化，可直接使用。

#### 1、处理Json的时间格式为正常格式：JsonDateTimeFormat

```c#
/// <summary>
/// 处理Json的时间格式为正常格式
/// </summary>
static string JsonDateTimeFormat(this string json)
```

#### 2、把对象序列化成Json字符串格式：ToJson

```c#
/// <summary>
/// 把对象序列化成Json字符串格式
/// </summary>
/// <param name="obj">Json 对象</param>
/// <param name="camelCase">是否小写名称</param>
/// <param name="indented"></param>
/// <returns>Json 字符串</returns>
static string ToJson(this object obj, bool camelCase = false, bool indented = false)
```

#### 3、把Json字符串转换为强类型对象：FromJson

```c#
/// <summary>
/// 把Json字符串转换为强类型对象
/// </summary>
static T FromJson<T>(this string json)
```

#### 4、反射对象深度拷贝：DeepCopy

```c#
/// <summary>
/// 反射对象深度拷贝
/// </summary>
/// <typeparam name="T">对象模型</typeparam>
/// <param name="obj">对象</param>
/// <returns></returns>
static T DeepCopy<T>(this T obj)
```

