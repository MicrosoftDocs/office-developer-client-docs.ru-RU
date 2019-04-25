---
title: Коллекция Parameters (DAO)
TOCTitle: Parameters Collection
ms:assetid: 52fc1ce4-7b3e-152d-7b6a-9c32a6470147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193967(v=office.15)
ms:contentKeyID: 48544862
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 09f60cb8dde407aacbb19e6b2124151dbbf9b3c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287897"
---
# <a name="parameters-collection-dao"></a><span data-ttu-id="468a0-102">Коллекция Parameters (DAO)</span><span class="sxs-lookup"><span data-stu-id="468a0-102">Parameters Collection (DAO)</span></span>

<span data-ttu-id="468a0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="468a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="468a0-104">Коллекция **Parameters** содержит все объекты **Parameter** объекта **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="468a0-104">A **Parameters** collection contains all the **Parameter** objects of a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="468a0-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="468a0-105">Remarks</span></span>

<span data-ttu-id="468a0-106">Коллекция **Parameters** предоставляет сведения только о существующих параметрах.</span><span class="sxs-lookup"><span data-stu-id="468a0-106">The **Parameters** collection provides information only about existing parameters.</span></span> <span data-ttu-id="468a0-107">Нельзя добавить объекты в коллекцию **Parameters** или удалить их из нее.</span><span class="sxs-lookup"><span data-stu-id="468a0-107">You can't append objects to or delete objects from the **Parameters** collection.</span></span>

## <a name="example"></a><span data-ttu-id="468a0-108">Пример</span><span class="sxs-lookup"><span data-stu-id="468a0-108">Example</span></span>

<span data-ttu-id="468a0-109">В этом примере демонстрируются объекты **Parameter** и коллекция **Parameters** путем создания временного объекта **QueryDef** и получения данных с учетом изменений, внесенных в **Parameters** объекта **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="468a0-109">This example demonstrates **Parameter** objects and the **Parameters** collection by creating a temporary **QueryDef** and retrieving data based on changes made to the **QueryDef** object's **Parameters**.</span></span> <span data-ttu-id="468a0-110">Процедура ParametersChange является обязательной для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="468a0-110">The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub ParameterX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfReport As QueryDef 
       Dim prmBegin As Parameter 
       Dim prmEnd As Parameter 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create temporary QueryDef object with two  
       ' parameters. 
       Set qdfReport = dbsNorthwind.CreateQueryDef("", _ 
          "PARAMETERS dteBegin DateTime, dteEnd DateTime; " & _ 
          "SELECT EmployeeID, COUNT(OrderID) AS NumOrders " & _ 
          "FROM Orders WHERE ShippedDate BETWEEN " & _ 
          "[dteBegin] AND [dteEnd] GROUP BY EmployeeID " & _ 
          "ORDER BY EmployeeID") 
       Set prmBegin = qdfReport.Parameters!dteBegin 
       Set prmEnd = qdfReport.Parameters!dteEnd 
     
       ' Print report using specified parameter values. 
       ParametersChange qdfReport, prmBegin, #1/1/95#, _ 
          prmEnd, #6/30/95# 
       ParametersChange qdfReport, prmBegin, #7/1/95#, _ 
          prmEnd, #12/31/95# 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Sub ParametersChange(qdfTemp As QueryDef, _ 
       prmFirst As Parameter, dteFirst As Date, _ 
       prmLast As Parameter, dteLast As Date) 
       ' Report function for ParameterX. 
     
       Dim rstTemp As Recordset 
       Dim fldLoop As Field 
     
       ' Set parameter values and open recordset from  
       ' temporary QueryDef object. 
       prmFirst = dteFirst 
       prmLast = dteLast 
       Set rstTemp = _  
          qdfTemp.OpenRecordset(dbOpenForwardOnly) 
       Debug.Print "Period " & dteFirst & " to " & dteLast 
     
       ' Enumerate recordset. 
       Do While Not rstTemp.EOF 
     
          ' Enumerate Fields collection of recordset. 
          For Each fldLoop In rstTemp.Fields 
             Debug.Print " - " & fldLoop.Name & " = " & fldLoop; 
          Next fldLoop 
     
          Debug.Print 
          rstTemp.MoveNext 
       Loop 
     
       rstTemp.Close 
     
    End Sub 
```

<br/>

В следующем примере показано, как создать запрос параметра. Запрос с именем **myQuery** создается с двумя параметрами: Param1 и Param2. <span data-ttu-id="468a0-113">Для этого в качестве свойства SQL запроса задается оператор языка SQL, определяющий параметры.</span><span class="sxs-lookup"><span data-stu-id="468a0-113">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="468a0-114">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="468a0-114">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="468a0-115">В приведенном ниже примере показано, как выполнить запрос параметра.</span><span class="sxs-lookup"><span data-stu-id="468a0-115">The following example shows how to execute a parameter query.</span></span> <span data-ttu-id="468a0-116">Коллекция Parameters используется, чтобы задать параметр Organization запроса myActionQuery перед его выполнением.</span><span class="sxs-lookup"><span data-stu-id="468a0-116">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="468a0-117">В приведенном ниже примере показано, как открыть объект Recordset на основании запроса параметра.</span><span class="sxs-lookup"><span data-stu-id="468a0-117">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```
