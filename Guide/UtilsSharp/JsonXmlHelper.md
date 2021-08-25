# UtilsSharp帮助类：JsonXmlHelper
`JsonXmlHelper`JsonXml帮助类共有以下几个方法

ben本类方法是静态方法无需实例化后使用，使用方法：

```c#
JsonXmlHelper.JsonToXml("{\"abc\":\"abc\"}")
```

#### 1、json转xml：JsonToXml

```c#
/// <summary>
/// json转xml
/// </summary>
/// <param name="json">json字符串</param>
/// <returns></returns>
static string JsonToXml(string json)
```

#### 2、xml转json：XmlToJson

```c#
/// <summary>
/// xml转json
/// </summary>
/// <param name="xml">xml字符串</param>
/// <returns></returns>
static string XmlToJson(string xml)
```

