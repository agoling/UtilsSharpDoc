# UtilsSharp帮助类：MathHelper

`MathHelper`数据计算辅助操作类

本类是静态类无需实例化，可直接使用。

#### 1、计算进度条进度：CalcProgress

```c#
/// <summary>
/// 计算进度条进度
/// </summary>
/// <param name="step">增加的量</param>
/// <param name="totalCount">总条数</param>
/// <param name="completeProgress">总完成进度</param>
/// <returns></returns>
static int CalcProgress(int step, int totalCount, int completeProgress = 100)
```

#### 2、获取两个坐标的距离：GetDistance

```c#
/// <summary>
/// 获取两个坐标的距离
/// </summary>
static double GetDistance(double x1, double y1, double x2, double y2)
```
