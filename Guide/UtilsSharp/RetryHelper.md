# UtilsSharp帮助类：RetryHelper
`RetryHelper`异常重试帮助类，本类满足大部分的异常重试，如果需要有更多扩展，可以在nuget搜索Polly安装使用,本类是静态方法，无需实例化直接使用。

#### 1、重试零个参数无返回值的方法：Execute

```c#
/// <summary>
/// 重试零个参数无返回值的方法
/// </summary>
/// <param name="action">执行方法方法</param>
/// <param name="retryInterval">重试间隔</param>
/// <param name="retryCount">重试次数</param>
static void Execute(Action action, TimeSpan retryInterval, int retryCount = 3)
```
#### 2、重试一个参数无返回值的方法：Execute

```c#
/// <summary>
/// 重试一个参数无返回值的方法
/// </summary>
/// <typeparam name="T1">参数类型1</typeparam>
/// <param name="action">执行方法方法</param>
/// <param name="arg1">参数1</param>
/// <param name="retryInterval">重试间隔</param>
/// <param name="retryCount">重试次数</param>
static void Execute<T1>(Action<T1> action, T1 arg1, TimeSpan retryInterval, int retryCount = 3)
```
#### 3、重试两个参数无返回值的方法：Execute

```c#
/// <summary>
/// 重试两个参数无返回值的方法
/// </summary>
/// <typeparam name="T1">参数类型1</typeparam>
/// <typeparam name="T2">参数类型2</typeparam>
/// <param name="action">执行方法方法</param>
/// <param name="arg1">参数1</param>
/// <param name="arg2">参数2</param>
/// <param name="retryInterval">重试间隔</param>
/// <param name="retryCount">重试次数</param>
static void Execute<T1, T2>(Action<T1, T2> action, T1 arg1, T2 arg2, TimeSpan retryInterval, int retryCount = 3)
```
#### 4、重试三个参数无返回值的方法：Execute

```c#
/// <summary>
/// 重试三个参数无返回值的方法
/// </summary>
/// <typeparam name="T1">参数类型1</typeparam>
/// <typeparam name="T2">参数类型2</typeparam>
/// <typeparam name="T3">参数类型3</typeparam>
/// <param name="action">执行方法方法</param>
/// <param name="arg1">参数1</param>
/// <param name="arg2">参数2</param>
/// <param name="arg3">参数3</param>
/// <param name="retryInterval">重试间隔</param>
/// <param name="retryCount">重试次数</param>
static void Execute<T1, T2, T3>(Action<T1, T2, T3> action, T1 arg1, T2 arg2, T3 arg3, TimeSpan retryInterval, int retryCount = 3)
```
#### 5、重试四个参数无返回值的方法：Execute

```c#
/// <summary>
/// 重试四个参数无返回值的方法
/// </summary>
/// <typeparam name="T1">参数类型1</typeparam>
/// <typeparam name="T2">参数类型2</typeparam>
/// <typeparam name="T3">参数类型3</typeparam>
/// <typeparam name="T4">参数类型4</typeparam>
/// <param name="action">执行方法方法</param>
/// <param name="arg1">参数1</param>
/// <param name="arg2">参数2</param>
/// <param name="arg3">参数3</param>
/// <param name="arg4">参数4</param>
/// <param name="retryInterval">重试间隔</param>
/// <param name="retryCount">重试次数</param>
static void Execute<T1, T2, T3, T4>(Action<T1, T2, T3, T4> action, T1 arg1, T2 arg2, T3 arg3, T4 arg4, TimeSpan retryInterval, int retryCount = 3)
```
#### 6、重试零个参数带返回值：Execute

```c#
/// <summary>
/// 重试零个参数带返回值
/// </summary>
/// <typeparam name="T">返回类型</typeparam>
/// <param name="func">执行的方法</param>
/// <param name="retryInterval">重试间隔</param>
/// <param name="retryCount">重试次数</param>
/// <returns>返回类型T</returns>
static T Execute<T>(Func<T> func, TimeSpan retryInterval, int retryCount = 3)
```
#### 7、重试一个参数带返回值：Execute

```c#
/// <summary>
/// 重试一个参数带返回值
/// </summary>
/// <typeparam name="T1">参数类型1</typeparam>
/// <typeparam name="T">返回类型</typeparam>
/// <param name="func">执行的方法</param>
/// <param name="arg1">参数1</param>
/// <param name="retryInterval">重试间隔</param>
/// <param name="retryCount">重试次数</param>
/// <returns>返回类型T</returns>
static T Execute<T1, T>(Func<T1, T> func, T1 arg1, TimeSpan retryInterval, int retryCount = 3)
```
#### 8、重试两个参数带返回值：Execute

```c#
/// <summary>
/// 重试两个参数带返回值
/// </summary>
/// <typeparam name="T1">参数类型1</typeparam>
/// <typeparam name="T2">参数类型2</typeparam>
/// <typeparam name="T">返回类型</typeparam>
/// <param name="func">执行的方法</param>
/// <param name="arg1">参数1</param>
/// <param name="arg2">参数2</param>
/// <param name="retryInterval">重试间隔</param>
/// <param name="retryCount">重试次数</param>
/// <returns>返回类型T</returns>
static T Execute<T1, T2, T>(Func<T1, T2, T> func, T1 arg1, T2 arg2, TimeSpan retryInterval, int retryCount = 3)
```
#### 9、重试三个参数带返回值：Execute

```c#
/// <summary>
/// 重试三个参数带返回值
/// </summary>
/// <typeparam name="T1">参数类型1</typeparam>
/// <typeparam name="T2">参数类型2</typeparam>
/// <typeparam name="T3">参数类型3</typeparam>
/// <typeparam name="T">返回类型</typeparam>
/// <param name="func">执行的方法</param>
/// <param name="arg1">参数1</param>
/// <param name="arg2">参数2</param>
/// <param name="arg3">参数3</param>
/// <param name="retryInterval">重试间隔</param>
/// <param name="retryCount">重试次数</param>
/// <returns>返回类型T</returns>
static T Execute<T1, T2, T3, T>(Func<T1, T2, T3, T> func, T1 arg1, T2 arg2, T3 arg3, TimeSpan retryInterval, int retryCount = 3)
```
#### 10、重试四个参数带返回值：Execute

```c#
/// <summary>
/// 重试四个参数带返回值
/// </summary>
/// <typeparam name="T1">参数类型1</typeparam>
/// <typeparam name="T2">参数类型2</typeparam>
/// <typeparam name="T3">参数类型3</typeparam>
/// <typeparam name="T4">参数类型4</typeparam>
/// <typeparam name="T">返回类型</typeparam>
/// <param name="func">执行的方法</param>
/// <param name="arg1">参数1</param>
/// <param name="arg2">参数2</param>
/// <param name="arg3">参数3</param>
/// <param name="arg4">参数4</param>
/// <param name="retryInterval">重试间隔</param>
/// <param name="retryCount">重试次数</param>
/// <returns>返回类型T</returns>
static T Execute<T1, T2, T3, T4, T>(Func<T1, T2, T3, T4, T> func, T1 arg1, T2 arg2, T3 arg3, T4 arg4, TimeSpan retryInterval, int retryCount = 3)
```