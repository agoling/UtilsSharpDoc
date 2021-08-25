# UtilsSharp帮助类：ImageHelper
`ImageHelper`图片帮助类主要是用来处理操作图片的，主要有：略缩图、图片水印、文字水印、调整光暗、反色处理、浮雕处理、拉伸图片、滤色处理、左右翻转、上下翻转、压缩图片、图片灰度化、转换为黑白图片、获取图片中的各帧等操作。

本类方法是静态方法无需实例化后使用

#### 1、Bitmap转bytes：BitmapToBytes

```c#
/// <summary>
/// Bitmap转bytes
/// </summary>
/// <param name="bitmap">bitmap</param>
/// <param name="imageFormat">图像格式</param>
/// <returns></returns>
static byte[] BitmapToBytes(Bitmap bitmap, ImageFormat imageFormat)
```

#### 2、图片转bytes：ImageToBytes

```c#
/// <summary>
/// 图片转bytes
/// </summary>
/// <param name="image">图片</param>
/// <returns></returns>
static byte[] ImageToBytes(Image image)
```

#### 3、bytes转Image：BytesToImage

```c#
/// <summary>
/// bytes转Image
/// </summary>
/// <param name="bytes">bytes</param>
/// <returns></returns>
static Image BytesToImage(byte[] bytes)
```

#### 4、 bytes生成并保存图片：CreateImageFromBytes

```c#
/// <summary>
/// bytes生成并保存图片
/// </summary>
/// <param name="path">图片路径</param>
/// <param name="bytes">bytes</param>
/// <returns></returns>
static string CreateImageFromBytes(string path, byte[] bytes)
```

#### 5、将图片旋转到正确位置：OrientationImage

```c#
/// <summary>
/// 将图片旋转到正确位置
/// 旋转角度  参数值
/// 0°	        1
/// 顺时针90°	  6
/// 逆时针90°	  8
/// 180°	    3
/// </summary>
/// <param name="image">图片对象</param>
/// <returns></returns>
static void OrientationImage(Image image)
```

#### 6、生成缩略图：MakeThumbnail

```c#
/// <summary>
/// 生成缩略图
/// </summary>
/// <param name="originalImagePath">源图路径（物理路径）</param>
/// <param name="thumbnailPath">缩略图路径（物理路径）</param>
/// <param name="width">缩略图宽度</param>
/// <param name="height">缩略图高度</param>
/// <param name="mode">生成缩略图的方式</param>    
static void MakeThumbnail(string originalImagePath, string thumbnailPath, int width, int height, MakeThumbnailMode mode)
```

#### 7、图片水印处理：ImageWatermark

```c#
/// <summary>
/// 图片水印处理
/// </summary>
/// <param name="path">需要加载水印的图片路径（绝对路径）</param>
/// <param name="waterpath">水印图片（绝对路径）</param>
/// <param name="location">水印位置（传送正确的代码）</param>
static string ImageWatermark(string path, string waterpath, string location)
```

#### 8、文字水印处理：LetterWatermark

```c#
/// <summary>
/// 文字水印处理
/// </summary>
/// <param name="path">图片路径（绝对路径）</param>
/// <param name="size">字体大小</param>
/// <param name="letter">水印文字</param>
/// <param name="color">颜色</param>
/// <param name="location">水印位置</param>
static string LetterWatermark(string path, int size, string letter, Color color, string location)
```

#### 9、调整光暗：LdPic

```c#
/// <summary>
/// 调整光暗
/// </summary>
/// <param name="mybm">原始图片</param>
/// <param name="width">原始图片的长度</param>
/// <param name="height">原始图片的高度</param>
/// <param name="val">增加或减少的光暗值</param>
static Bitmap LdPic(Bitmap mybm, int width, int height, int val)
```

#### 10、反色处理：RePic

```c#
/// <summary>
/// 反色处理
/// </summary>
/// <param name="mybm">原始图片</param>
/// <param name="width">原始图片的长度</param>
/// <param name="height">原始图片的高度</param>
static Bitmap RePic(Bitmap mybm, int width, int height)
```

#### 11、浮雕处理：Fd

```c#
/// <summary>
/// 浮雕处理
/// </summary>
/// <param name="oldBitmap">原始图片</param>
/// <param name="width">原始图片的长度</param>
/// <param name="height">原始图片的高度</param>
static Bitmap Fd(Bitmap oldBitmap, int width, int height)
```

#### 12、拉伸图片：ResizeImage

```c#
/// <summary>
/// 拉伸图片
/// </summary>
/// <param name="bmp">原始图片</param>
/// <param name="newW">新的宽度</param>
/// <param name="newH">新的高度</param>
static Bitmap ResizeImage(Bitmap bmp, int newW, int newH)
```

#### 13、滤色处理：FilPic

```c#
/// <summary>
/// 滤色处理
/// </summary>
/// <param name="mybm">原始图片</param>
/// <param name="width">原始图片的长度</param>
/// <param name="height">原始图片的高度</param>
static Bitmap FilPic(Bitmap mybm, int width, int height)
```

#### 14、左右翻转：RevPicLr

```c#
/// <summary>
/// 左右翻转
/// </summary>
/// <param name="mybm">原始图片</param>
/// <param name="width">原始图片的长度</param>
/// <param name="height">原始图片的高度</param>
static Bitmap RevPicLr(Bitmap mybm, int width, int height)
```

#### 15、上下翻转：RevPicUd

```c#
/// <summary>
/// 上下翻转
/// </summary>
/// <param name="mybm">原始图片</param>
/// <param name="width">原始图片的长度</param>
/// <param name="height">原始图片的高度</param>
static Bitmap RevPicUd(Bitmap mybm, int width, int height)
```

#### 16、压缩图片到指定尺寸：Compress

```c#
/// <summary>
/// 压缩图片到指定尺寸
/// </summary>
/// <param name="oldfile">原文件</param>
/// <param name="newfile">新文件</param>
static bool Compress(string oldfile, string newfile)
```

#### 17、图片灰度化：Gray

```c#
/// <summary>
/// 图片灰度化
/// </summary>
/// <param name="c">颜色</param>
/// <returns></returns>
static Color Gray(Color c)
```

#### 18、转换为黑白图片：BwPic

```c#
/// <summary>
/// 转换为黑白图片
/// </summary>
/// <param name="mybm">要进行处理的图片</param>
/// <param name="width">图片的长度</param>
/// <param name="height">图片的高度</param>
static Bitmap BwPic(Bitmap mybm, int width, int height)
```

#### 19、获取图片中的各帧：GetFrames

```c#
/// <summary>
/// 获取图片中的各帧
/// </summary>
/// <param name="pPath">图片路径</param>
/// <param name="pSavedPath">保存路径</param>
static void GetFrames(string pPath, string pSavedPath)
```

