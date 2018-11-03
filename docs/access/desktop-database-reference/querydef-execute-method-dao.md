---
title: Метод QueryDef.Execute (DAO)
TOCTitle: Execute Method
ms:assetid: ad9e859e-c6fe-496c-a1f2-a000cf4bebcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821728(v=office.15)
ms:contentKeyID: 48547043
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052884
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 165a2703b3b3715ace7326df31477f1f9293be12
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926215"
---
# <a name="querydefexecute-method-dao"></a><span data-ttu-id="f1b2e-102">Метод QueryDef.Execute (DAO)</span><span class="sxs-lookup"><span data-stu-id="f1b2e-102">QueryDef.Execute method (DAO)</span></span>

<span data-ttu-id="f1b2e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1b2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1b2e-104">Выполняет инструкции SQL на указанный объект.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-104">Executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b2e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1b2e-105">Syntax</span></span>

<span data-ttu-id="f1b2e-106">*выражение* . Выполнение (***Параметры***)</span><span class="sxs-lookup"><span data-stu-id="f1b2e-106">*expression* .Execute(***Options***)</span></span>

<span data-ttu-id="f1b2e-107">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="f1b2e-107">*expression* A variable that represents a **QueryDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="f1b2e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1b2e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1b2e-109">Имя</span><span class="sxs-lookup"><span data-stu-id="f1b2e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f1b2e-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="f1b2e-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f1b2e-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f1b2e-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="f1b2e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f1b2e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1b2e-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1b2e-113">Options</span></span></p></td>
<td><p><span data-ttu-id="f1b2e-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="f1b2e-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="f1b2e-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f1b2e-115"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f1b2e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1b2e-116">Remarks</span></span>

<span data-ttu-id="f1b2e-117">Следующие константы **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** можно использовать для доступа к параметрам.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-117">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for Options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1b2e-118">Константа</span><span class="sxs-lookup"><span data-stu-id="f1b2e-118">Constant</span></span></p></th>
<th><p><span data-ttu-id="f1b2e-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f1b2e-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1b2e-120"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="f1b2e-120"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="f1b2e-121">Запрещает разрешение на запись другим пользователям (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f1b2e-121">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b2e-122"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="f1b2e-122"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="f1b2e-123">(По умолчанию) Выполняет несогласованных обновлений (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f1b2e-123">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b2e-124"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="f1b2e-124"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="f1b2e-125">Выполняет согласованности обновлений (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f1b2e-125">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b2e-126"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="f1b2e-126"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="f1b2e-127">Выполняет запрос к серверу.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-127">Executes an SQL pass-through query.</span></span> <span data-ttu-id="f1b2e-128">Если этот параметр передает инструкции SQL к базе данных ODBC для обработки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f1b2e-128">Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b2e-129"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="f1b2e-129"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="f1b2e-130">Откат обновления при возникновении ошибки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f1b2e-130">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b2e-131"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="f1b2e-131"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="f1b2e-132">Создает ошибку времени выполнения, если другой пользователь изменение данных, редактировании (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f1b2e-132">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b2e-133"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="f1b2e-133"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="f1b2e-134">Выполняет асинхронный запрос (только объекты технология ODBCDirect подключения и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="f1b2e-134">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b2e-135"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="f1b2e-135"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="f1b2e-136">Выполняет оператор без первого вызова функции SQLPrepare ODBC API (только объекты технология ODBCDirect подключения и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="f1b2e-136">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="f1b2e-137">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-137">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="f1b2e-138">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-138">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="f1b2e-139">Константы **dbConsistent** и **dbInconsistent** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-139">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive.</span></span> <span data-ttu-id="f1b2e-140">Можно использовать одно или другое, но не оба в экземпляре **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-140">You can use one or the other, but not both in a given instance of **OpenRecordset**.</span></span> <span data-ttu-id="f1b2e-141">С помощью **dbConsistent** и **dbInconsistent** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-141">Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="f1b2e-142">Используйте свойство **[RecordsAffected](querydef-recordsaffected-property-dao.md)** объекта **[подключения](connection-object-dao.md)**, **[базы данных](database-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** для определения количества записей, влияет на последнюю метод **[Execute](querydef-execute-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="f1b2e-142">Use the **[RecordsAffected](querydef-recordsaffected-property-dao.md)** property of the **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)**, or **[QueryDef](querydef-object-dao.md)** object to determine the number of records affected by the most recent **[Execute](querydef-execute-method-dao.md)** method.</span></span> <span data-ttu-id="f1b2e-143">Например **RecordsAffected** содержит число записей удален, обновляется или вставляется при выполнении запроса.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-143">For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query.</span></span> <span data-ttu-id="f1b2e-144">При использовании метода **Execute** для выполнения запроса, свойство **RecordsAffected** объекта **QueryDef** присваивается количество записей.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-144">When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="f1b2e-145">В рабочей области Microsoft Access, если предоставить синтаксически правильные инструкции SQL и имеют соответствующие разрешения метода **Execute** не ошибка — даже в том случае, если не одной строки можно изменить или удалить.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-145">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted.</span></span> <span data-ttu-id="f1b2e-146">Таким образом всегда используйте параметр **dbFailOnError** , при использовании метода **Execute** для запуска и обновления или удаления запроса.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-146">Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query.</span></span> <span data-ttu-id="f1b2e-147">Этот параметр, возникает ошибка времени выполнения и выполняет откат всех изменений успешно Если никакой из записей влияет на блокируется и не может быть обновлении или удалении.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-147">This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="f1b2e-148">В более ранних версиях ядра базы данных Microsoft Jet SQL операторы автоматически были внедрены в неявные транзакции.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-148">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions.</span></span> <span data-ttu-id="f1b2e-149">Если не удалось выполнить инструкции, с **dbFailOnError** , всей оператор будет выполнен откат.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-149">If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back.</span></span> <span data-ttu-id="f1b2e-150">В целях повышения производительности эти неявные транзакции были удалены, начиная с версии 3.5.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-150">To improve performance, these implicit transactions were removed starting with version 3.5.</span></span> <span data-ttu-id="f1b2e-151">При обновлении старых кода DAO, необходимо принять во внимание использование явных транзакций вокруг **выполнение** инструкций.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-151">If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="f1b2e-152">Для достижения наилучшей производительности в рабочую область для Microsoft Access, особенно в многопользовательской среде вложить метода **Execute** внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-152">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction.</span></span> <span data-ttu-id="f1b2e-153">Используйте метод **[BeginTrans](workspace-begintrans-method-dao.md)** на текущий объект **[рабочей области](workspace-object-dao.md)** , а затем используйте метод **Execute** и завершения транзакции с помощью метода **[CommitTrans](workspace-committrans-method-dao.md)** в **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-153">Use the **[BeginTrans](workspace-begintrans-method-dao.md)** method on the current **[Workspace](workspace-object-dao.md)** object, then use the **Execute** method, and complete the transaction by using the **[CommitTrans](workspace-committrans-method-dao.md)** method on the **Workspace**.</span></span> <span data-ttu-id="f1b2e-154">Это сохраняет изменения на диске и освобождает любые блокировки во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-154">This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="f1b2e-155">Пример</span><span class="sxs-lookup"><span data-stu-id="f1b2e-155">Example</span></span>

<span data-ttu-id="f1b2e-156">В этом примере демонстрируется использование метода **Execute** при вызове из объекта **QueryDef** и объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="f1b2e-156">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object.</span></span> <span data-ttu-id="f1b2e-157">Процедуры ExecuteQueryDef и PrintOutput необходимы для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-157">The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

```vb
    Sub ExecuteX() 
     
       Dim dbsNorthwind As Database 
       Dim strSQLChange As String 
       Dim strSQLRestore As String 
       Dim qdfChange As QueryDef 
       Dim rstEmployees As Recordset 
       Dim errLoop As Error 
     
       ' Define two SQL statements for action queries. 
       strSQLChange = "UPDATE Employees SET Country = " & _ 
          "'United States' WHERE Country = 'USA'" 
       strSQLRestore = "UPDATE Employees SET Country = " & _ 
          "'USA' WHERE Country = 'United States'" 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Create temporary QueryDef object. 
       Set qdfChange = dbsNorthwind.CreateQueryDef("", _ 
          strSQLChange) 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "SELECT LastName, Country FROM Employees", _ 
          dbOpenForwardOnly) 
     
       ' Print report of original data. 
       Debug.Print _ 
          "Data in Employees table before executing the query" 
       PrintOutput rstEmployees 
        
       ' Run temporary QueryDef. 
       ExecuteQueryDef qdfChange, rstEmployees 
        
       ' Print report of new data. 
       Debug.Print _ 
          "Data in Employees table after executing the query" 
       PrintOutput rstEmployees 
     
       ' Run action query to restore data. Trap for errors, 
       ' checking the Errors collection if necessary. 
       On Error GoTo Err_Execute 
       dbsNorthwind.Execute strSQLRestore, dbFailOnError 
       On Error GoTo 0 
     
       ' Retrieve the current data by requerying the recordset. 
       rstEmployees.Requery 
     
       ' Print report of restored data. 
       Debug.Print "Data after executing the query " & _ 
          "to restore the original information" 
       PrintOutput rstEmployees 
     
       rstEmployees.Close 
        
       Exit Sub 
        
    Err_Execute: 
     
       ' Notify user of any errors that result from 
       ' executing the query. 
       If DBEngine.Errors.Count > 0 Then 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
       End If 
        
       Resume Next 
     
    End Sub 
     
    Sub ExecuteQueryDef(qdfTemp As QueryDef, _ 
       rstTemp As Recordset) 
     
       Dim errLoop As Error 
        
       ' Run the specified QueryDef object. Trap for errors, 
       ' checking the Errors collection if necessary. 
       On Error GoTo Err_Execute 
       qdfTemp.Execute dbFailOnError 
       On Error GoTo 0 
     
       ' Retrieve the current data by requerying the recordset. 
       rstTemp.Requery 
        
       Exit Sub 
     
    Err_Execute: 
     
       ' Notify user of any errors that result from 
       ' executing the query. 
       If DBEngine.Errors.Count > 0 Then 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
       End If 
        
       Resume Next 
     
    End Sub 
     
    Sub PrintOutput(rstTemp As Recordset) 
     
       ' Enumerate Recordset. 
       Do While Not rstTemp.EOF 
          Debug.Print "  " & rstTemp!LastName & _ 
             ", " & rstTemp!Country 
          rstTemp.MoveNext 
       Loop 
     
    End Sub 
```

<br/>

<span data-ttu-id="f1b2e-158">Приведенный ниже показано, как выполнить запрос параметра.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-158">The following example shows how to execute a parameter query.</span></span> <span data-ttu-id="f1b2e-159">Коллекции параметров используется для задания параметра организации запроса myActionQuery до выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="f1b2e-159">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="f1b2e-160">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="f1b2e-160">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
