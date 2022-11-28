# UtilsSharp帮助类：NumberHelper

`NumberHelper`数字帮助类帮助类

本类是静态类无需实例化，可直接使用。

#### 1、阿拉伯数字转中文数字(仅支持0~10)：ToCnNumber

```c#
/// <summary>
/// 阿拉伯数字转中文数字(仅支持0~10)
/// </summary>
/// <param name="num">数字(仅支持0~10)</param>
/// <param name="capitalization">是否返回大写中文数字</param>
/// <returns></returns>
static string ToCnNumber(int num, bool capitalization = false)
```

#### 2、金额转中文大写整数支持到万亿,小数部分支持到分(超过两位将进行Banker舍入法处理)：ToCnMoney

```c#
/// <summary>
/// 金额转中文大写整数支持到万亿,小数部分支持到分(超过两位将进行Banker舍入法处理)
/// </summary>
/// <param name="num">需要转换的双精度浮点数</param>
/// <returns></returns>
static BaseResult<string> ToCnMoney(double num)
```

#### 3、金额以元和万元为单位：ToUnitMoney

```c#
/// <summary>
/// 金额以元和万元为单位
/// </summary>
/// <param name="num">需转换的金额</param>
/// <returns></returns>
static string ToUnitMoney(decimal num)
```

