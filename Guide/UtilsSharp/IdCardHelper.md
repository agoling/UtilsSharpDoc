# UtilsSharp帮助类：IdCardHelper

`IdCardHelper`身份证相关验证帮助类

本类是静态类无需实例化，可直接使用。

#### 1、身份证号码验证（判断是否是正确的身份证号码）：IsIdCard

```c#
/// <summary>
///  身份证号码验证（判断是否是正确的身份证号码）
/// </summary>
/// <param name="idCardNumber">15或18位身份证</param>
/// <returns></returns>
static BaseResult<bool> IsIdCard(string idCardNumber)
```

#### 2、获取出生日期（yyyy-MM-dd）：GetIdCardBirthday

```c#
/// <summary>
/// 获取出生日期（yyyy-MM-dd）
/// </summary>
/// <param name="idCardNumber">身份证号码</param>
/// <returns></returns>
static BaseResult<string> GetIdCardBirthday(string idCardNumber)
```

#### 3、获取性别：GetIdCardSex

```c#
/// <summary>
/// 获取性别
/// </summary>
/// <param name="idCardNumber">身份证号码</param>
/// <returns>男/女</returns>
static BaseResult<string> GetIdCardSex(string idCardNumber)
```

#### 4、获取身份证全部信息：GetIdCardInfo

```c#
/// <summary>
/// 获取身份证全部信息
/// </summary>
/// <param name="idCardNumber">身份证号码</param>
/// <returns></returns>
static BaseResult<string> GetIdCardInfo(string idCardNumber)
```

#### 5、获取随机身份证号码：GetIdCardRandomNum

```c#
/// <summary>
/// 获取随机身份证号码
/// </summary>
/// <param name="type"></param>
/// <param name="data"></param>
/// <returns>身份证号码</returns>
static BaseResult<string> GetIdCardRandomNum(int type, string data)
```

#### 6、获取户籍所在地：GetIdCardAddress

```c#
/// <summary>
/// 获取户籍所在地
/// </summary>
/// <param name="idCardNumber">身份证号码</param>
/// <returns></returns>
static BaseResult<string> GetIdCardAddress(string idCardNumber)
```

