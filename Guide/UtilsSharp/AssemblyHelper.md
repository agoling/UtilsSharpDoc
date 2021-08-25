# UtilsSharp帮助类：AssemblyHelper
`AssemblyHelper`程序集帮助类，主要有以下方法：

本类方法是静态方法无需实例化后使用

#### 1、获取类以及类实现的接口键值对：GetClassInterfacePairs

```c#
/// <summary>
/// 获取类以及类实现的接口键值对
/// </summary>
/// <param name="assemblyName">程序集名称</param>
/// <returns>类以及类实现的接口键值对</returns>
static Dictionary<Type, List<Type>> GetClassInterfacePairs(string assemblyName)
```

#### 2、获取所有的程序集(排除所有的系统程序集、Nuget下载包)：GetAssemblies

```c#
/// <summary>
/// 获取所有的程序集(排除所有的系统程序集、Nuget下载包)
/// </summary>
/// <returns>程序集集合</returns>
static List<Assembly> GetAssemblies()
```

#### 3、获取所有的程序集(含所有系统程序集、Nuget下载包)：GetAllAssemblies

```c#
/// <summary>
/// 获取所有的程序集(含所有系统程序集、Nuget下载包)
/// </summary>
/// <returns>程序集集合</returns>
static List<Assembly> GetAllAssemblies()
```

#### 4、获取指定的程序集(模糊匹配)：GetAssembly

```c#
/// <summary>
/// 获取指定的程序集(模糊匹配)
/// </summary>
/// <param name="assemblyName">程序集名称</param>
/// <returns>程序集</returns>
static Assembly GetAssembly(string assemblyName)
```

