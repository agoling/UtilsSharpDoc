# UtilsSharp帮助类：WinCmdHelper
`WinCmdHelper`windows命令帮助类共有以下几个方法

本类方法是静态方法无需实例化后使用，使用方法：

```c#
WinCmdHelper.RunCommand("xxxx",false,false)
```

#### 1、执行Dos命令：RunCommand

```c#
/// <summary>
/// 执行Dos命令
/// </summary>
/// <param name="cmd">Dos命令及参数</param>
/// <param name="isShowCmdWindow">是否显示cmd窗口</param>
/// <param name="isCloseCmdProcess">执行完毕后是否关闭cmd进程</param>
/// <returns></returns>
static BaseResult<string> RunCommand(string cmd, bool isShowCmdWindow, bool isCloseCmdProcess)
```

#### 2、判断指定的进程是否在运行中：IsProcessExists

```c#
/// <summary>
/// 判断指定的进程是否在运行中
/// </summary>
/// <param name="processName">要判断的进程名称，不包括扩展名exe</param>
/// <param name="processFileName">进程文件的完整路径</param>
/// <returns>存在返回true，否则返回false</returns>
static bool IsProcessExists(string processName, string processFileName)
```

#### 3、结束指定的windows进程如果进程存在：KillProcess

```c#
/// <summary>
/// 结束指定的windows进程如果进程存在
/// </summary>
/// <param name="processName">进程名称，不包含扩展名</param>
/// <param name="processFileName">进程文件完整路径，如果为空则删除所有进程名为processName参数值的进程</param>
static BaseResult<string> KillProcess(string processName, string processFileName)
```

