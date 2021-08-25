# UtilsSharp帮助类：DataTableHelper

`DataTableHelper`帮助类共有以下几个方法

本类无需实例化后使用，使用方法：

#### 1、 DataTable转实体：ToEntity

```c#
/// <summary>
/// DataTable转实体
/// </summary>
/// <typeparam name="T">实体</typeparam>
/// <param name="table">DataTable实例</param>
/// <returns></returns>
static T ToEntity<T>(this DataTable table) where T : new()
```

#### 2、DataTable转实体集合：ToEntities

```c#
/// <summary>
///  DataTable转实体集合
/// </summary>
/// <typeparam name="T">实体</typeparam>
/// <param name="table">DataTable实例</param>
/// <returns></returns>
static List<T> ToEntities<T>(this DataTable table) where T : new()
```

#### 3、指定集合转DataTable：ToDataTable

```c#
/// <summary>
/// 指定集合转DataTable
/// </summary>
/// <param name="list">指定集合</param>
/// <returns></returns>
static DataTable ToDataTable(this IList list)
```

#### 4、指定实体集合转DataTable：ToDataTable

```c#
/// <summary>
/// 指定实体集合转DataTable
/// </summary>
/// <typeparam name="T">实体</typeparam>
/// <param name="list">实体集合</param>
/// <returns></returns>
static DataTable ToDataTable<T>(this List<T> list)
```

