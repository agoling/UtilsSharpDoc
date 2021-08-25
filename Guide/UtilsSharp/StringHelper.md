# UtilsSharp帮助类：StringHelper
`StringHelper`字符串帮助类共有以下几个方法，本类方法是静态方法无需实例化后使用

#### 1、需要全局注册下本方法，可以支持.Net平台上不支持的编码，如GB2312：EncodingRegister

```c#
/// <summary>
///需要全局注册下本方法，可以支持.Net平台上不支持的编码，如GB2312
/// </summary>
static void EncodingRegister()
```

#### 2、 转义正则表达式特殊符号：TransferenceRegex

```c#
/// <summary>
/// 转义正则表达式特殊符号
/// </summary>
/// <param name="str">字符串</param>
/// <returns></returns>
static string TransferenceRegex(string str)
```

#### 3、过滤Html符号：HtmlToTxt

```c#
/// <summary>
/// 过滤Html符号
/// </summary>
/// <param name="htmlStr">html字符串</param>
/// <returns></returns>
static string HtmlToTxt(string htmlStr)
```

#### 4、获取字符串长度：GetCharLength

```c#
/// <summary>
/// 获取字符串长度
/// </summary>
/// <param name="str">字符串</param>
/// <returns></returns>
static int GetCharLength(string str)
```

#### 5、按字符长度截取字符串：CutChar

```c#
/// <summary>
/// 按字符长度截取字符串
/// </summary>
/// <param name="str">字符串</param>
/// <param name="charLength">要截取的字符长度</param>
/// <returns></returns>
static string CutChar(string str, int charLength)
```

#### 6、按字长度截取字符串：CutString

```c#
/// <summary>
/// 按字长度截取字符串
/// </summary>
/// <param name="str">字符串</param>
/// <param name="strCount">要截取的字数（含）</param>
/// <returns></returns>
static string CutString(string str, int strCount)
```

#### 7、 字符串分割获取项：SplitString

```c#
/// <summary>
/// 字符串分割获取项
/// </summary>
/// <param name="str">例如："苹果,香蕉,猕猴桃,凤梨,枇杷,葡萄,柠檬,橘子,火龙果"</param>
/// <param name="splitChar">,</param>
/// <param name="returnItemCount">2</param>
/// <returns>苹果,香蕉</returns>
static string SplitString(string str, char splitChar, int returnItemCount)
```

#### 8、反转字符串：Reverse

```c#
/// <summary>
/// 反转字符串
/// </summary>
/// <param name="str">字符串</param>
/// <returns></returns>
static string Reverse(string str)
```

#### 9、压缩字符串：Compress

```c#
/// <summary>
/// 压缩字符串
/// </summary>
/// <param name="str">字符串</param>
/// <param name="encoding">编码</param>
/// <returns></returns>
static string Compress(string str,Encoding encoding=null)
```

#### 10、字符串解压缩：DeCompress

```c#
/// <summary>
///  字符串解压缩
/// </summary>
/// <param name="str">字符串</param>
/// <param name="encoding">编码</param>
/// <returns></returns>
static string DeCompress(string str, Encoding encoding = null)
```

#### 11、隐藏手机号(手机号加星星如：136****8568)：HideMobilePhone

```c#
/// <summary>
/// 隐藏手机号(手机号加星星如：136****8568)
/// </summary>
/// <param name="mobilePhone">手机号</param>
/// <returns></returns>
static string HideMobilePhone(string mobilePhone)
```

