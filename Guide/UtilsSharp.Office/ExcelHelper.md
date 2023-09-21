# UtilsSharp.Office帮助类：ExcelHelper
`ExcelHelper`Excel帮助类是为了简化数据的导入导出，导入和导出都有两种方式，一种数据源是DataTable，另外一种数据源是List数据集，支持xls和xlsx两种格式的文件。

本类使用方法：

#### 1、数据导入：DataTableToExcel

```c#
using UtilsSharp;

/// <summary>
/// DataTable方式导入
/// </summary>
public static void Import()
{
    var list = new List<UserInfo>();
    list.Add(new UserInfo() { Name = "小A", Email = "11", Password = "12", Phone = "13", IsHappy = true, Age = 14, BirthTime = DateTime.Now.AddYears(-20) });
    list.Add(new UserInfo() { Name = "小B", Email = "21", Password = "22", Phone = "23", IsHappy = false, Age = 15, BirthTime = DateTime.Now.AddYears(-15) });
    list.Add(new UserInfo() { Name = "小C", Email = "这篇文章主要为大家详细介绍了C#使用NPOI导出Excel类封装", Password = "32", Phone = "33", IsHappy = true, Age = 16, BirthTime = DateTime.Now.AddYears(-30) });

    var filePath1 = "d:\\1.xlsx";

    var dt = DataTableHelper.ToDataTable(list);
    //DataTable方式 导入
    ExcelHelper.DataTableToExcel(dt, filePath1);
}
```

#### 2、数据导入：ListToExcel

```c#
/// <summary>
/// List方式导入
/// </summary>
public static void Import()
{
    var list = new List<UserInfo>();
    list.Add(new UserInfo() { Name = "小A", Email = "11", Password = "12", Phone = "13", IsHappy = true, Age = 14, BirthTime = DateTime.Now.AddYears(-20) });
    list.Add(new UserInfo() { Name = "小B", Email = "21", Password = "22", Phone = "23", IsHappy = false, Age = 15, BirthTime = DateTime.Now.AddYears(-15) });
    list.Add(new UserInfo() { Name = "小C", Email = "这篇文章主要为大家详细介绍了C#使用NPOI导出Excel类封装", Password = "32", Phone = "33", IsHappy = true, Age = 16, BirthTime = DateTime.Now.AddYears(-30) });

    var filePath1 = "d:\\1.xlsx";

    //List方式 导入
    ExcelHelper.ListToExcel(list, filePath1);
}
```

#### 3、数据导出：ExcelToDataTable

```c#
/// <summary>
/// DataTable方式导出
/// </summary>
public static void Export()
{
    var filePath1 = "d:\\1.xlsx";    
    var dt = ExcelHelper.ExcelToDataTable(filePath1);
}
```

#### 4、数据导出：ExcelToList

```c#
 /// <summary>
 /// 数据导出
 /// </summary>
 public static void Export()
 {
     var filePath1 = "d:\\1.xlsx";
     var list = ExcelHelper.ExcelToList<UserInfo>(filePath1);
 }
```
