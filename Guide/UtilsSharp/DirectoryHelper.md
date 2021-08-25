# UtilsSharp帮助类：DirectoryHelper
`DirectoryHelper`文件夹帮助类共有以下几个方法

本类方法是静态方法无需实例化后使用，使用方法：

```c#
DirectoryHelper.ConvertToDirectory("dir/20210816/")
```

#### 1、获取桌面目录路径：GetDesktopDirectory

```c#
/// <summary>
/// 获取桌面目录路径
/// </summary>
/// <returns></returns>
static string GetDesktopDirectory()
```

#### 2、得到绝对目录路径：ConvertToDirectory

```c#
/// <summary>
/// 得到绝对目录路径
/// </summary>
/// <param name="dirPath">目录路径如：dir/{DateTime.Now.Date:yyyy-MM-dd}/ </param>
/// <returns></returns>
static string ConvertToDirectory(string dirPath)
```

