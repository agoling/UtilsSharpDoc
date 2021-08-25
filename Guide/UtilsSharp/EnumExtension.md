# UtilsSharp帮助类：EnumExtension

`EnumExtension`是枚举扩展类。

本扩展类是静态类，可直接使用。

#### 1、字符串值转换为枚举值：ToEnum

```c#
/// <summary>
/// 字符串值转换为枚举值
/// </summary>
/// <typeparam name="T">枚举</typeparam>
/// <param name="value">枚举值不区分(字符串)</param>
/// <returns></returns>
static T ToEnum<T>(this string value) where T : Enum
```

#### 2、数字值转换为枚举值：ToEnum

```c#
/// <summary>
/// 数字值转换为枚举值
/// </summary>
/// <typeparam name="T">枚举</typeparam>
/// <param name="value">枚举值(数值)</param>
/// <returns></returns>
static T ToEnum<T>(this int value) where T : Enum
```

#### 3、判断某个值是否定义在枚举中：IsDefined

```c#
/// <summary>
/// 判断某个值是否定义在枚举中
/// </summary>
/// <typeparam name="T">枚举</typeparam>
/// <param name="value">值</param>
/// <returns></returns>
static bool IsDefined<T>(this object value) where T : Enum
```

#### 4、 获取枚举的描述信息：GetEnumDescription

```c#
/// <summary>
/// 获取枚举的描述信息
/// </summary>
/// <param name="en">枚举对象</param>
/// <returns></returns>
static string GetEnumDescription(this Enum en)
```

#### 5、枚举转List：EnumToList

```c#
/// <summary>
/// 枚举转List
/// </summary>
/// <typeparam name="T">枚举对象</typeparam>
/// <returns></returns>
static List<EnumEntity> EnumToList<T>()
```

