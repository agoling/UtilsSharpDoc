# UtilsSharp帮助类：MapperHelper

`MapperHelper`对象与对象映射帮助类

本类是静态类无需实例化，可直接使用。

#### 1、将对象TSource转换为TTarget：Map

```c#
/// <summary>
/// 将对象TSource转换为TTarget
/// </summary>
/// <param name="source">对象</param>
/// <returns></returns>
static TTarget Map(TSource source)
```

#### 2、将对象TSource的值赋给给TTarget：Map

```c#
/// <summary>
/// 将对象TSource的值赋给给TTarget
/// </summary>
/// <param name="source">源对象</param>
/// <param name="target">结果对象</param>
static void Map(TSource source, TTarget target)
```

#### 3、将对象TSource集合转换为TTarget集合：MapList

```c#
/// <summary>
/// 将对象TSource集合转换为TTarget集合
/// </summary>
/// <param name="sources">对象集合</param>
/// <returns></returns>
static List<TTarget> MapList(IEnumerable<TSource> sources)
```

