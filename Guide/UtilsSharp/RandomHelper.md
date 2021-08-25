# UtilsSharp帮助类：RandomHelper
`RandomHelper`随机相关帮助类，可支持生成随机数字、随机数字与字母混合、随机字母、随机排序list数据、生成不重复的随机数值、随机时间等

本类方法是静态方法无需实例化后使用，使用方法：

```c#
var num=RandomHelper.Number(5)
```

#### 1、生成随机数字：Number

```c#
/// <summary>
/// 生成随机数字
/// </summary>
/// <param name="length">生成长度</param>
static string Number(int length)
```

```c#
/// <summary>
/// 生成随机数字
/// </summary>
/// <param name="length">生成长度</param>
/// <param name="sleep">是否要在生成前将当前线程阻止以避免重复</param>
static string Number(int length, bool sleep)
```

#### 2、生成随机数字与字母：NumberAndLetters

```c#
/// <summary>
/// 生成随机数字与字母
/// </summary>
/// <param name="length">生成长度</param>
static string NumberAndLetters(int length)
```

```c#
/// <summary>
/// 生成随机数字与字母
/// </summary>
/// <param name="length">生成长度</param>
/// <param name="sleep">是否要在生成前将当前线程阻止以避免重复</param>
static string NumberAndLetters(int length, bool sleep)
```

#### 3、生成随机字母(只有字母)：Letters

```c#
/// <summary>
/// 生成随机字母(只有字母)
/// </summary>
/// <param name="length">生成长度</param>
static string Letters(int length)
```

```c#
/// <summary>
/// 生成随机字母(只有字母)
/// </summary>
/// <param name="length">生成长度</param>
/// <param name="sleep">是否要在生成前将当前线程阻止以避免重复</param>
static string Letters(int length, bool sleep)
```

#### 4、随机排序list数据：ListData

```c#
/// <summary>
///  随机排序list数据
/// </summary>
/// <typeparam name="T">对象</typeparam>
/// <param name="data">数据</param>
/// <returns></returns>
static List<T> ListData<T>(List<T> data)
```

#### 5、生成不重复的随机数值：NumbersNoRepeating

```c#
/// <summary>
/// 生成不重复的随机数值
/// </summary>
/// <param name="minValue">最小值</param>
/// <param name="maxValue">最大值</param>
/// <returns></returns>
static int[] NumbersNoRepeating(int minValue, int maxValue)
```

#### 6、生成随机时间：Time

```c#
/// <summary>
/// 生成随机时间
/// </summary>
/// <param name="time1">起始时间</param>
/// <param name="time2">结束时间</param>
/// <returns>间隔时间之间的 随机时间</returns>
static DateTime Time(DateTime time1, DateTime time2)
```

