# UtilsSharp帮助类：DingTalkRobot
`DingTalkRobot`钉钉自定义机器人帮助类共有以下几个方法

本类方法是静态方法无需实例化后使用，使用方法：

#### 1、调用自定义机器人发Text类型消息：SendTextMessage

```c#
/// <summary>
///  调用自定义机器人发Text类型消息
/// </summary>
/// <param name="webhook">webHook地址</param>
/// <param name="content">消息内容</param>
/// <param name="atMobiles">被@人的手机号</param>
/// <param name="isAtAll">@所有人时:true,否则为:false</param>
/// <returns></returns>
static BaseResult<object> SendTextMessage(string webhook, string content, List<string> atMobiles, bool isAtAll)
```

#### 2、调用自定义机器人发Link类型消息：SendLinkMessage

```c#
/// <summary>
/// 调用自定义机器人发Link类型消息
/// </summary>
/// <param name="webhook">webHook地址</param>
/// <param name="title">消息标题</param>
/// <param name="text">消息内容(注：如果太长只会部分展示)</param>
/// <param name="picUrl">图片url</param>
/// <param name="messageUrl">点击消息跳转的url</param>
/// <returns></returns>
static BaseResult<object> SendLinkMessage(string webhook, string title, string text, string picUrl, string messageUrl)
```

#### 3、调用自定义机器人发Markdown类型消息：SendMarkdownMessage

```c#
/// <summary>
/// 调用自定义机器人发Markdown类型消息
/// </summary>
/// <param name="webhook">webHook地址</param>
/// <param name="title">消息标题</param>
/// <param name="titleType">标题类型等级</param>
/// <param name="markdownMessages">消息内容</param>
/// <param name="atMobiles">被@手机号</param>
/// <param name="isAtAll">@所有人时:true,否则为:false</param>
/// <returns></returns>
static BaseResult<object> SendMarkdownMessage(string webhook, string title, TitleType titleType, List<MarkdownMessage> markdownMessages, List<string> atMobiles, bool isAtAll)
```

#### 4、调用自定义机器人发整体跳转ActionCard类型消息：SendActionCardMessage

```c#
/// <summary>
/// 调用自定义机器人发整体跳转ActionCard类型消息
/// </summary>
/// <param name="webhook">webHook地址</param>
/// <param name="title">消息标题</param>
/// <param name="markdownMessages">消息内容</param>
/// <param name="hideAvatar">0-正常发消息者头像,1-隐藏发消息者头像</param>
/// <param name="btnOrientation">0-按钮竖直排列，1-按钮横向排列</param>
/// <param name="singleTitle">单个按钮的方案。(设置此项和singleUrl后btns无效。)</param>
/// <param name="singleUrl">点击singleTitle按钮触发的URL</param>
/// <returns></returns>
static BaseResult<object> SendActionCardMessage(string webhook, string title, List<MarkdownMessage> markdownMessages, int hideAvatar, int btnOrientation, string singleTitle, string singleUrl)
```

#### 5、调用自定义机器人发独立跳转ActionCard类型消息：SendSingleActionCardMessage

```c#
/// <summary>
/// 调用自定义机器人发独立跳转ActionCard类型消息
/// </summary>
/// <param name="webhook">webHook地址</param>
/// <param name="title">消息标题</param>
/// <param name="markdownMessages">消息内容</param>
/// <param name="hideAvatar">0-正常发消息者头像,1-隐藏发消息者头像</param>
/// <param name="btnOrientation">0-按钮竖直排列，1-按钮横向排列</param>
/// <param name="btns">按钮集合</param>
/// <returns></returns>
static BaseResult<object> SendSingleActionCardMessage(string webhook, string title, List<MarkdownMessage> markdownMessages, int hideAvatar, int btnOrientation, List<Btn> btns)
```

#### 6、调用自定义机器人发FeedCard类型消息：SendFeedCardMessage

```c#
/// <summary>
/// 调用自定义机器人发FeedCard类型消息
/// </summary>
/// <param name="webhook">webHook地址</param>
/// <param name="links">图片按钮集合</param>
/// <returns></returns>
static BaseResult<object> SendFeedCardMessage(string webhook, List<Link> links)
```

