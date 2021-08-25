# UtilsSharp帮助类：ChinaDate

`ChinaDate`是公历农历相关类

本类方法是静态方法，无需实例化，可直接使用：

#### 1、传回公历y年m月的总天数：GetDaysByMonth

```c#
/// <summary>
/// 传回公历y年m月的总天数
/// </summary>
/// <param name="y">年</param>
/// <param name="m">月</param>
/// <returns></returns>
static int GetDaysByMonth(int y, int m)
```

#### 2、根据日期值获得周一的日期：GetMondayDateByDate

```c#
/// <summary>
/// 根据日期值获得周一的日期
/// </summary>
/// <param name="dt">输入日期</param>
/// <returns>周一的日期</returns>
static DateTime GetMondayDateByDate(DateTime dt)
```

#### 3、根据时间获取农历信息：GetChinaDate

```c#
/// <summary>
/// 根据时间获取农历信息
/// </summary>
/// <param name="dt">时间</param>
/// <returns></returns>
static CNDate GetChinaDate(DateTime dt)
```

