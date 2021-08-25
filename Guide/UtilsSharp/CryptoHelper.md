# UtilsSharp帮助类：CryptoHelper

`CryptoHelper`加密解密帮助类共有6种加密方式，分别是MD5加密、DES加密解密、RSA加密解密、SHA不可逆加密、Base64加密解密、AES加密解密。

本类是静态类无需实例化，可直接使用。

#### 1、MD5加密：ToMd5

```c#
/// <summary>
/// MD5加密
/// </summary>
/// <param name="str">加密字符串</param>
/// <returns></returns>
static string ToMd5(this string str)
```

#### 2、DES加密：ToDesEncrypt

```c#
/// <summary>
/// DES加密
/// </summary>
/// <param name="str">加密字符串</param>
/// <param name="secretKey">密文</param>
/// <param name="iv">向量</param>
/// <returns>加密后的字符串</returns>
static string ToDesEncrypt(this string str, string secretKey, string iv)
```

#### 3、DES解密：ToDesDecrypt

```c#
/// <summary>
/// DES解密
/// </summary>
/// <param name="str">解密字符串</param>
/// <param name="secretKey">密文</param>
/// <param name="iv">向量</param>
/// <returns>解密后的字符串</returns>
static string ToDesDecrypt(this string str, string secretKey, string iv)
```

#### 4、RSA加密：ToRsaEncrypt

默认密钥是：UtilsSharp

```c#
/// <summary> 
/// RSA加密 
/// </summary> 
/// <param name="str">加密字符串</param> 
/// <param name="secretKey">密文</param> 
/// <returns></returns> 
static string ToRsaEncrypt(this string str, string secretKey)
```

#### 5、RSA解密：ToRsaDecrypt

默认密钥是：UtilsSharp

```c#
/// <summary> 
/// RSA解密 
/// </summary> 
/// <param name="str">解密字符串</param> 
/// <param name="secretKey">密匙容器的名称</param> 
/// <returns></returns> 
static string ToRsaDecrypt(this string str, string secretKey)
```

#### 6、SHA不可逆加密之SHA1加密：ToSha1Encrypt

```c#
/// <summary>
/// SHA1加密
/// </summary>
/// <param name="str">加密字符串</param>
/// <returns></returns>
static string ToSha1Encrypt(this string str)
```

#### 7、SHA不可逆加密之SHA256加密：ToSha256Encrypt

```c#
/// <summary>
/// SHA256加密
/// </summary>
/// <param name="str">加密字符串</param>
/// <returns></returns>
static string ToSha256Encrypt(this string str)
```

#### 8、SHA不可逆加密之SHA384加密：ToSha384Encrypt

```c#
/// <summary>
/// SHA384加密
/// </summary>
/// <param name="str">加密字符串</param>
/// <returns></returns>
static string ToSha384Encrypt(this string str)
```

#### 9、SHA不可逆加密之SHA512加密：ToSha512Encrypt

```c#
/// <summary>
/// SHA512加密
/// </summary>
/// <param name="str">加密字符串</param>
/// <returns></returns>
static string ToSha512Encrypt(this string str)
```

#### 10、Base64加密：ToBase64Encrypt

```c#
/// <summary>
/// Base64加密
/// </summary>
/// <param name="str">需要加密的字符串</param>
/// <returns></returns>
static string ToBase64Encrypt(this string str)
```

#### 11、Base64加密(指定字符编码)：ToBase64Encrypt

```c#
/// <summary>
/// Base64加密(指定字符编码)
/// </summary>
/// <param name="str">需要加密的字符串</param>
/// <param name="encode">字符编码</param>
/// <returns></returns>
static string ToBase64Encrypt(this string str, Encoding encode)
```

#### 12、Base64解密：ToBase64Decrypt

```c#
/// <summary>
/// Base64解密
/// </summary>
/// <param name="str">需要解密的字符串</param>
/// <returns></returns>
static string ToBase64Decrypt(this string str)
```

#### 13、Base64解密(指定字符编码)：ToBase64Decrypt

```c#
/// <summary>
/// Base64解密(指定字符编码)
/// </summary>
/// <param name="str">需要解密的字符串</param>
/// <param name="encode">字符的编码</param>
/// <returns></returns>
static string ToBase64Decrypt(this string str, Encoding encode)
```

#### 14、AES加密：ToAesEncrypt

```c#
/// <summary>
///  AES加密
/// </summary>
/// <param name="str">明文（待加密）</param>
/// <param name="secretKey">密文</param>
/// <returns></returns>
static string ToAesEncrypt(this string str, string secretKey)
```

#### 15、AES解密：ToAesDecrypt

```c#
/// <summary>
///  AES解密
/// </summary>
/// <param name="str">明文（待解密）</param>
/// <param name="secretKey">密文</param>
/// <returns></returns>
static string ToAesDecrypt(this string str, string secretKey)
```

