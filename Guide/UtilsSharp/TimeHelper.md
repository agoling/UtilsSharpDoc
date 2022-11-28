# UtilsSharp帮助类：TimeHelper
`TimeHelper`时间相关帮助类共有以下几个方法

本类方法是静态方法无需实例化后使用，使用方法：

```c#
DateTime dt=DateTime.Now();
var startDate=TimeHelper.GetUtcStartDate(dt);
```

#### 1、获取开始日期(UTC)：GetUtcStartDate

搜索列表的时候，经常会用到获取搜索的起始时间和结束时间，本例子是获取起始时间，获取到的时间格式是”YYYY-MM-DD 00:00:00“,时区转换过。

```c#
/// <summary>
/// 获取开始日期(UTC)
/// </summary>
/// <param name="dateTime">时间</param>
/// <returns></returns>
static DateTime GetUtcStartDate(DateTime dateTime)
```

#### 2、 获取开始日期：GetStartDate

搜索列表的时候，经常会用到获取搜索的起始时间和结束时间，本例子是获取起始时间，获取到的时间格式是”YYYY-MM-DD 00:00:00“,时区未转换过。
```c#
/// <summary>
/// 获取开始日期
/// </summary>
/// <param name="dateTime">时间</param>
/// <returns></returns>
static DateTime GetStartDate(DateTime dateTime)
```
#### 3、 获取结束日期(UTC)：GetUtcEndDate

搜索列表的时候，经常会用到获取搜索的起始时间和结束时间，本例子是获取结束时间，获取到的时间格式是”YYYY-MM-DD 23:59:59“,时区转换过。
```c#
/// <summary>
/// 获取结束日期(UTC)
/// </summary>
/// <param name="dateTime">时间</param>
/// <returns></returns>
static DateTime GetUtcEndDate(DateTime dateTime)
```
#### 4、 获取结束日期：GetEndDate

搜索列表的时候，经常会用到获取搜索的起始时间和结束时间，本例子是获取起始时间，获取到的时间格式是”YYYY-MM-DD 23:59:59“,时区未转换过。
```c#
/// <summary>
/// 获取结束日期
/// </summary>
/// <param name="dateTime">时间</param>
/// <returns></returns>
static DateTime GetEndDate(DateTime dateTime)
```
#### 5、时间格式化(小时分钟前面加上0)：TimeWithZero

这个就是在时间的前面加个0，比如当前的Hour是5，通过这个方法后，值变为05
```c#
/// <summary>
/// 时间格式化(小时分钟前面加上0)
/// </summary>
/// <param name="intStr">小时、分钟</param>
/// <returns>"00"</returns>
static string TimeWithZero(string intStr)
```
#### 6、时间格式化(小时分钟去掉前面的0)：TimeTrimZero

这个就是在时间的前面移除0，比如当前的Hour是05，通过这个方法后，值变为5
```c#
/// <summary>
/// 时间格式化(小时分钟去掉前面的0)
/// </summary>
/// <param name="intStr">小时、分钟</param>
/// <returns>0</returns>
static int TimeTrimZero(string intStr)
```
#### 7、返回某年某月最后一天：GetMonthLastDate
```c#
/// <summary>
/// 返回某年某月最后一天
/// </summary>
/// <param name="year">年份</param>
/// <param name="month">月份</param>
/// <returns>日</returns>
static int GetMonthLastDate(int year, int month)
```
#### 8、获取时间差字符串：GetDateDiff

这个方法主要的作用就是返回字符串的时间差，比如xx秒前、xx分钟前、xx小时前等
```c#
/// <summary>
/// 获取时间差字符串
/// </summary>
/// <param name="time1">起始时间</param>
/// <param name="time2">结束时间</param>
/// <returns></returns>
static string GetDateDiff(DateTime time1, DateTime time2)
```
#### 9、获得两个日期的间隔：GetTimeSpan
```c#
/// <summary>
/// 获得两个日期的间隔
/// </summary>
/// <param name="time1">起始日期</param>
/// <param name="time2">结束日期</param>
/// <returns>日期间隔TimeSpan。</returns>
static TimeSpan GetTimeSpan(DateTime time1, DateTime time2)
```
#### 10、中文版指定一周的某天：ChinaDayOfWeek

```c#
/// <summary>
/// 中文版指定一周的某天
/// </summary>
/// <param name="dateTime">时间</param>
/// <returns></returns>
static string ChinaDayOfWeek(DateTime dateTime)
```

```c#
/// <summary>
/// 中文版指定一周的某天
/// </summary>
/// <param name="dayOfWeek">指定一周的某天</param>
/// <returns></returns>
static string ChinaDayOfWeek(DayOfWeek dayOfWeek)
```

#### 11、时间戳转DateTime：TimeStampToDateTime
```c#
/// <summary>
/// 时间戳转DateTime
/// </summary>
/// <param name="timeStamp">时间戳</param>
/// <param name="type">类型：秒，毫秒</param>
/// <returns></returns>
static DateTime TimeStampToDateTime(string timeStamp, TimeStampType type= TimeStampType.秒)
```
#### 12、DateTime转时间戳：DateTimeToTimeStamp
```c#
/// <summary>
/// DateTime转时间戳
/// </summary>
/// <param name="dateTime">DateTime</param>
/// <param name="type">类型：秒，毫秒</param>
/// <returns></returns>
static long DateTimeToTimeStamp(DateTime dateTime, TimeStampType type = TimeStampType.秒)
```
#### 13、获取指定日期，在为一年中为第几周：GetWeekOfYear
```c#
/// <summary>
/// 获取指定日期，在为一年中为第几周
/// </summary>
/// <param name="dt">指定时间</param>
/// <reutrn>返回第几周</reutrn>
static int GetWeekOfYear(DateTime dt)
```

#### 14、当前时间是否周末：IsWeekend

```c#
/// <summary>
/// 当前时间是否周末
/// </summary>
/// <param name="dateTime">时间点</param>
/// <returns></returns>
static bool IsWeekend(DateTime dateTime)
```

#### 15、当前时间是否工作日：IsWeekday

```c#
/// <summary>
/// 当前时间是否工作日
/// </summary>
/// <param name="dateTime">时间点</param>
/// <returns></returns>
static bool IsWeekday(DateTime dateTime)
```

