# UtilsSharp帮助类：FileHelper

`FileHelper`文件操作帮助类,包含以下几个方法：

本类方法是静态方法无需实例化后使用，使用方法：

```c#
FileHelper.ReadFileToBytes("D://xxxx")
```

#### 1、读取文件到byte[]：ReadFileToBytes

```c#
/// <summary>
/// 读文件到byte[]
/// </summary>
/// <param name="fileName">硬盘文件路径</param>
/// <returns></returns>
static byte[] ReadFileToBytes(string fileName)
```

#### 2、读取文件到stream：ReadFileToStream

```c#
/// <summary>
/// 读取文件到Stream
/// </summary>
/// <param name="fileName">硬盘文件路径</param>
/// <returns></returns>
static Stream ReadFileToStream(string fileName)
```

#### 3、写byte[]到fileName：WriteBytesToFile

```c#
/// <summary>
/// 写byte[]到fileName
/// </summary>
/// <param name="bytes">byte[]</param>
/// <param name="fileName">保存至硬盘路径</param>
/// <returns></returns>
static bool WriteBytesToFile(byte[] bytes, string fileName)
```

#### 4、stream转为byte[]：StreamToBytes

```c#
/// <summary>
/// stream转为byte[]
/// </summary>
/// <param name="stream">参数</param>
/// <returns></returns>
static byte[] StreamToBytes(Stream stream)
```

#### 5、byte[] 转为stream：BytesToStream

```c#
/// <summary>
/// byte[] 转为stream
/// </summary>
/// <param name="bytes">参数</param>
/// <returns></returns>
static Stream BytesToStream(byte[] bytes)
```

