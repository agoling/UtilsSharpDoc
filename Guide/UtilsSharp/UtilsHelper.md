# UtilsSharp帮助类：UtilsHelper
`UtilsHelper`公共工具帮助类共有以下几个方法

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

#### 2、反射对象深度拷贝：DeepCopy

```c#
/// <summary>
/// 反射对象深度拷贝
/// </summary>
/// <typeparam name="T">对象模型</typeparam>
/// <param name="obj">对象</param>
/// <returns></returns>
static T DeepCopy<T>(this T obj)
```

