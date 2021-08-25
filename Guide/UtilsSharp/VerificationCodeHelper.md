# UtilsSharp帮助类：VerificationCodeHelper

`VerificationCodeHelper`验证码生成帮助类，主要是用来生成数字字母图片验证码用。

本类需要实例化后使用，使用方法如下：

```c#
var rule = new VerificationCodeRule 
{
  LetterCount = 4,//验证码位数
  LetterWidth = 16,//单个字体的宽度范围
  LetterHeight = 20//单个字体的高度范围
};
var vcHelper=new VerificationCodeHelper(rule);
var code= vcHelper.Text;//验证码
var image = vcHelper.Image;//验证码图片
```

#### 1、公共属性两个：Text和Image，Text是验证码，Image是验证码图片

#### 2、绘制验证码：CreateImage

```c#
/// <summary>
/// 绘制验证码
/// </summary>
/// <param name="rule">绘制规则</param>
void CreateImage(VerificationCodeRule rule)
```

#### 3、字体随机颜色：GetRandomColor

```c#
/// <summary>
/// 字体随机颜色
/// </summary>
Color GetRandomColor()
```

#### 4、正弦曲线Wave扭曲图片：TwistImage

```c#
/// <summary>
/// 正弦曲线Wave扭曲图片
/// </summary>
/// <param name="srcBmp">图片路径</param>
/// <param name="bXDir">如果扭曲则选择为True</param>
/// <param name="waveformValue">波形的幅度倍数，越大扭曲的程度越高,一般为3</param>
/// <param name="dPhase">波形的起始相位,取值区间[0-2*PI)</param>
Bitmap TwistImage(Bitmap srcBmp, bool bXDir, double waveformValue, double dPhase)
```