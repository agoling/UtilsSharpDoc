# UtilsSharp帮助类：RegexHelper
`RegexHelper`正则匹配帮助类共有以下几个方法
本类方法是静态方法无需实例化后使用，使用方法：
```c#
var isMatch=RegexHelper.IsMatch("xxxxxx","xxx");
```

#### 1、正则是否匹配:IsMatch

```c#
/// <summary>
/// 正则是否匹配
/// </summary>
/// <param name="input">字符串</param>
/// <param name="pattern">正则规则</param>
/// <returns></returns>
static bool IsMatch(string input,string pattern)
```

```c#
/// <summary>
/// 正则是否匹配
/// </summary>
/// <param name="input">字符串</param>
/// <param name="pattern">正则规则</param>
/// <param name="options">提供用于设置正则表达式选项的枚举值</param>
/// <returns></returns>
static bool IsMatch(string input, string pattern,RegexOptions options)
```

#### 2、从指定字符串中过滤出符合正则匹配的字符串:Match

```c#
/// <summary>
/// 从指定字符串中过滤出符合正则匹配的字符串
/// </summary>
/// <param name="input">字符串</param>
/// <param name="pattern">正则规则</param>
/// <returns></returns>
static GroupCollection Match(string input, string pattern)
```

```c#
/// <summary>
/// 从指定字符串中过滤出符合正则匹配的字符串
/// </summary>
/// <param name="input">字符串</param>
/// <param name="pattern">正则规则</param>
/// <param name="options">提供用于设置正则表达式选项的枚举值</param>
/// <returns></returns>
static GroupCollection Match(string input, string pattern, RegexOptions options)
```

#### 3、从指定字符串中过滤出所有符合正则匹配的子集:Matches

```c#
/// <summary>
/// 从指定字符串中过滤出所有符合正则匹配的子集
/// </summary>
/// <param name="input">字符串</param>
/// <param name="pattern">正则规则</param>
/// <returns></returns>
static List<GroupCollection> Matches(string input, string pattern)
```

```c#
/// <summary>
/// 从指定字符串中过滤出所有符合正则匹配的子集
/// </summary>
/// <param name="input">字符串</param>
/// <param name="pattern">正则规则</param>
/// <param name="options">提供用于设置正则表达式选项的枚举值</param>
/// <returns></returns>
static List<GroupCollection> Matches(string input, string pattern, RegexOptions options)
```

#### 4、验证IP地址是否合法，如果为空认为验证不合格:IsIp

```c#
/// <summary>
/// 验证IP地址是否合法，如果为空认为验证不合格
/// </summary>
/// <param name="ip">要验证的IP地址</param>        
static bool IsIp(string ip)
```

#### 5、验证手机号码是否合法，如果为空认为验证不合格:IsMobile

```c#
/// <summary>
/// 验证手机号码是否合法，如果为空认为验证不合格
/// </summary>
/// <param name="mobile">要验证的手机号码</param>        
static bool IsMobile(string mobile)
```

#### 6、验证EMail是否合法，如果为空认为验证不合格：IsEmail

```c#
/// <summary>
/// 验证EMail是否合法，如果为空认为验证不合格
/// </summary>
/// <param name="email">要验证的Email</param>
static bool IsEmail(string email)
```

#### 7、验证是否为整数，如果为空认为验证不合格：IsInt

```c#
/// <summary>
/// 验证是否为整数，如果为空认为验证不合格
/// </summary>
/// <param name="number">要验证的整数</param>        
static bool IsInt(string number)
```

#### 8、验证是否为数字，如果为空认为验证不合格：IsNumber

```c#
/// <summary>
/// 验证是否为数字，如果为空认为验证不合格
/// </summary>
/// <param name="number">要验证的数字</param>        
static bool IsNumber(string number)
```

#### 9、验证日期是否合法,如果为空认为验证不合格：IsDate

```c#
/// <summary>
/// 验证日期是否合法,如果为空认为验证不合格
/// </summary>
/// <param name="date">日期</param>
static bool IsDate(ref string date)
```

#### 10、验证身份证是否合法，如果为空认为验证不合格：IsIdCard

```c#
//该接口已经转到 IdCardHelper
```

#### 11、检测客户输入的字符串是否有效：IsValidInput

检测客户输入的字符串是否有效,并将原始字符串修改为有效字符串或空字符串

当检测到客户的输入中有攻击性危险字符串,则返回false,有效返回true

```c#
/// <summary>
/// 检测客户输入的字符串是否有效,并将原始字符串修改为有效字符串或空字符串
/// 当检测到客户的输入中有攻击性危险字符串,则返回false,有效返回true
/// </summary>
/// <param name="input">要检测的字符串</param>
static bool IsValidInput(ref string input)
```

