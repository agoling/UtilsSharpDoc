# UtilsSharp帮助类：ChinesePinyinHelper

`ChinesePinyinHelper`汉字拼音帮助类,包含以下几个方法：

本类方法是静态方法无需实例化后使用，使用方法：

```c#
ChinesePinyinHelper.GetPinyinInitials("xxx")
```

#### 1、获取汉字拼音的首字母：GetPinyinInitials

```c#
/// <summary>
/// 获取汉字拼音的首字母
/// </summary>
/// <param name="chineseStr">汉字字符串</param>
/// <returns></returns>
static string GetPinyinInitials(string chineseStr)
```

#### 2、获取汉字拼音：GetPinyin

```c#
/// <summary>
/// 获取汉字拼音
/// </summary>
/// <param name="chineseStr">汉字字符串</param>
/// <returns></returns>
string GetPinyin(string chineseStr)
```