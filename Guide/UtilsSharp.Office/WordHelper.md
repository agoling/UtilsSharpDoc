# UtilsSharp.Office帮助类：WordHelper
`WordHelper`word帮助类是为了简化word数据的导出，支持文字、图片、表格的插入并导出word文件

本类需要实例化后使用，使用方法：

```c#
WordHelper wordHelper = new WordHelper();
```

#### 1、Word数据导出例子

```c#
 /// <summary>
 /// Word文档生成
 /// </summary>
 public static void Word()
 {
     //表格数据集
     var list = new List<UserInfo>();
     list.Add(new UserInfo() { Name = "小A", Email = "11", Password = "12", Phone = "13", IsHappy = true, Age = 14, BirthTime = DateTime.Now.AddYears(-20) });
     list.Add(new UserInfo() { Name = "小B", Email = "21", Password = "22", Phone = "23", IsHappy = false, Age = 15, BirthTime = DateTime.Now.AddYears(-15) });
     list.Add(new UserInfo() { Name = "小C", Email = "这篇文章主要为大家详细介绍了C#使用NPOI导出Excel类封装", Password = "32", Phone = "33", IsHappy = true, Age = 16, BirthTime = DateTime.Now.AddYears(-30) });
    
     WordHelper wordHelper = new WordHelper();
     //插入大标题
     wordHelper.InsertTitle("我是大标题");
     //插入副标题
     wordHelper.InsertSubTitle("我是附标题");
     //插入内容
     wordHelper.InsertContent("这篇文章主要为大家详细介绍了C#使用NPOI导出Excel类封装，文中示例代码介绍的非常详细，具有一定的参考价值，感兴趣的小伙伴们可以参考一下");
     //插入本地图片
     wordHelper.InsertLocalImage("d:\\21.jpg", "我的图片");
     wordHelper.InsertContent("NPOI是指构建在POI 3.x版本之上的一个程序，NPOI可以在没有安装Office的情况下对Word或Excel文档进行读写操作。 NPOI是一个开源的C#读写Excel、WORD等微软OLE2组件文档的项目。");
     //插入标题
     wordHelper.InsertTable(list);
     //换行
     wordHelper.InsertWrap();
     //插入在线图片
     wordHelper.InsertOnlineImage("https://cbu01.alicdn.com/img/ibank/O1CN01o7Vgv224q1zQmDfyP_!!2209334127441-0-cib.jpg", "我的图片");
     wordHelper.InsertContent("以下代码主要分3部分：通过实体类");
     var request1 = new WordTextRequest()
     {
         Text = "您好",
         FontName = "Arial",
         FontSize = 12,
         Color = "red",
         IsBold = false,
         IsItalic = false,
         Underline = UnderlinePatterns.None
     };
     var request2 = new WordTextRequest()
     {
         Text = "老师",
         FontName = "Arial",
         FontSize = 12,
         Color = "green",
         IsBold = false,
         IsItalic = false,
         Underline = UnderlinePatterns.WavyHeavy
     };

     var wordTextRequests = new List<WordTextRequest>();
     wordTextRequests.Add(request1);
     wordTextRequests.Add(request2);

     //追加方式插入内容，该种方式支持在一段话中加入不同的文字样式
     wordHelper.AppendContent(wordTextRequests);
     //删除含“构建”词语的段落
     wordHelper.DeleteParagraph("构建");
     //把文档中含有“标题”的字替换为“主题0591”
     wordHelper.ReplaceText("标题", "主题0591");
     //保存文档；注意：保存文档的时候，文档如果已经有内容会被覆盖，另外文档保存时，不能被另外程序使用，比如在wps打开等
     wordHelper.Save("d:\\3.doc");

 }
```

