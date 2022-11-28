# UtilsSharp帮助类：DirectoryHelper
`DirectoryHelper`文件夹帮助类共有以下几个方法

本类方法是静态方法无需实例化后使用，使用方法：

```c#
DirectoryHelper.ConvertToDirectory("dir/20210816/")
```

#### 1、创建文件夹，如果不存在：CreateIfNotExists

```c#
/// <summary>
/// 创建文件夹，如果不存在
/// </summary>
/// <param name="dirPath">要创建的文件夹路径</param>
static void CreateIfNotExists(string dirPath)
```


#### 2、递归复制文件夹及文件夹/文件：Copy

```c#
/// <summary>
/// 递归复制文件夹及文件夹/文件
/// </summary>
/// <param name="sourcePath"> 源文件夹路径 </param>
/// <param name="targetPath"> 目的文件夹路径 </param>
/// <param name="searchPatterns"> 要复制的文件扩展名数组 </param>
static void Copy(string sourcePath, string targetPath, string[] searchPatterns = null)
```


#### 3、递归删除目录：Delete

```c#
/// <summary>
/// 递归删除目录
/// </summary>
/// <param name="dirPath"> 目录路径 </param>
/// <param name="isDeleteRoot"> 是否删除根目录 </param>
/// <returns> 是否成功 </returns>
static bool Delete(string dirPath, bool isDeleteRoot = true)
```


#### 4、设置或取消目录的FileAttributes属性：SetAttributes

```c#
/// <summary>
/// 设置或取消目录的<see cref="FileAttributes"/>属性。
/// </summary>
/// <param name="dirPath">目录路径</param>
/// <param name="attribute">要设置的目录属性</param>
/// <param name="isSet">true为设置，false为取消</param>
static void SetAttributes(string dirPath, FileAttributes attribute, bool isSet)
```


#### 5、获取程序根目录路径：GetRootDirectory

```c#
/// <summary>
/// 获取程序根目录路径
/// </summary>
static string GetRootDirectory()
```


#### 6、获取桌面目录路径：GetDesktopDirectory

```c#
/// <summary>
/// 获取桌面目录路径
/// </summary>
/// <returns></returns>
static string GetDesktopDirectory()
```


#### 7、得到绝对目录路径：ConvertToDirectory

```c#
/// <summary>
/// 得到绝对目录路径
/// </summary>
/// <param name="dirPath">目录路径如：dir/{DateTime.Now.Date:yyyy-MM-dd}/ </param>
/// <returns></returns>
static string ConvertToDirectory(string dirPath)
```

