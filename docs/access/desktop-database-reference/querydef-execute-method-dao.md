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
localization_priority: Priority
ms.openlocfilehash: 7ef7f61ef632617b8d64a3fd9c34e5887e50065c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302963"
---
# <a name="querydefexecute-method-dao"></a><span data-ttu-id="407da-102">Метод QueryDef.Execute (DAO)</span><span class="sxs-lookup"><span data-stu-id="407da-102">QueryDef.Execute Method (DAO)</span></span>

<span data-ttu-id="407da-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="407da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="407da-104">Выполняет инструкцию SQL для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="407da-104">Executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="407da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="407da-105">Syntax</span></span>

<span data-ttu-id="407da-106">*выражение* .Execute(***Options***)</span><span class="sxs-lookup"><span data-stu-id="407da-106">*expression* .Execute(***Options***)</span></span>

<span data-ttu-id="407da-107">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="407da-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="407da-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="407da-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="407da-109">Имя</span><span class="sxs-lookup"><span data-stu-id="407da-109">Name</span></span></p></th>
<th><p><span data-ttu-id="407da-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="407da-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="407da-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="407da-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="407da-112">Описание</span><span class="sxs-lookup"><span data-stu-id="407da-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="407da-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="407da-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="407da-114">Необязательно</span><span class="sxs-lookup"><span data-stu-id="407da-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="407da-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="407da-115"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="407da-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="407da-116">Remarks</span></span>

<span data-ttu-id="407da-117">В параметре Options можно использовать перечисленные ниже константы **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="407da-117">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for Options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="407da-118">Константа</span><span class="sxs-lookup"><span data-stu-id="407da-118">Constant</span></span></p></th>
<th><p><span data-ttu-id="407da-119">Описание</span><span class="sxs-lookup"><span data-stu-id="407da-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="407da-120"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="407da-120"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="407da-121">Отказывает в разрешении на запись другим пользователям (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="407da-121">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407da-122"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="407da-122"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="407da-123">(По умолчанию) Выполняет несогласованные обновления (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="407da-123">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="407da-124"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="407da-124"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="407da-125">Выполняет согласованные обновления (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="407da-125">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407da-126"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="407da-126"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="407da-127">Выполняет SQL-запрос к серверу.</span><span class="sxs-lookup"><span data-stu-id="407da-127">Executes an SQL pass-through query.</span></span> <span data-ttu-id="407da-128">При установке этого параметра инструкция SQL передается в базу данных ODBC для обработки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="407da-128">Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="407da-129"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="407da-129"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="407da-130">Выполняет откат обновлений, если возникает ошибка (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="407da-130">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407da-131"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="407da-131"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="407da-132">Создает ошибку во время выполнения, если другой пользователь пытается изменить данные, которые вы редактируете (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="407da-132">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="407da-133"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="407da-133"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="407da-134">Выполняет запрос асинхронно (только для объектов ODBCDirect Connection и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="407da-134">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407da-135"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="407da-135"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="407da-136">Выполняет инструкцию, не вызывая перед этим функцию API ODBC SQLPrepare (только для объектов ODBCDirect Connection и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="407da-136">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="407da-137">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="407da-137">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="407da-138">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="407da-138">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="407da-139">Константы **dbConsistent** и **dbInconsistent** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="407da-139">NOTE: The constants **dbConsistent** and **dbInconsistent** are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="407da-140">В том или ином экземпляре **OpenRecordset** можно использовать любую из них, но не обе.</span><span class="sxs-lookup"><span data-stu-id="407da-140">You can use one or the other, but not both in a given instance of **OpenRecordset**.</span></span> <span data-ttu-id="407da-141">Одновременное использование **dbConsistent** и **dbInconsistent** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="407da-141">Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="407da-142">Свойство **[RecordsAffected](querydef-recordsaffected-property-dao.md)** объекта **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** используется для определения числа записей, затронутых самым последним вызовом метода **[Execute](querydef-execute-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="407da-142">Use the **[RecordsAffected](querydef-recordsaffected-property-dao.md)** property of the **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)**, or **[QueryDef](querydef-object-dao.md)** object to determine the number of records affected by the most recent **[Execute](querydef-execute-method-dao.md)** method.</span></span> <span data-ttu-id="407da-143">Например, **RecordsAffected** содержит число записей, удаленных, обновленных или вставленных при выполнении запроса на изменение.</span><span class="sxs-lookup"><span data-stu-id="407da-143">For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query.</span></span> <span data-ttu-id="407da-144">Если метод **Execute** используется для выполнения запроса, в качестве значения свойства **RecordsAffected** объекта **QueryDef** устанавливается число затронутых записей.</span><span class="sxs-lookup"><span data-stu-id="407da-144">When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="407da-145">Когда в рабочей области Microsoft Access указана синтаксически правильная инструкция SQL и имеются соответствующие разрешения, метод **Execute** не приводит к сбою, даже если не удается изменить или удалить ни одну строку.</span><span class="sxs-lookup"><span data-stu-id="407da-145">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted.</span></span> <span data-ttu-id="407da-146">Поэтому всегда используйте параметр **dbFailOnError** при применении метода **Execute** для обновления или удаления запроса.</span><span class="sxs-lookup"><span data-stu-id="407da-146">Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query.</span></span> <span data-ttu-id="407da-147">Этот параметр создает ошибку во время выполнения и откатывает все успешно выполненные изменения, если какие-либо затронутые записи заблокированы и не могут быть обновлены или удалены.</span><span class="sxs-lookup"><span data-stu-id="407da-147">This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="407da-148">В более ранних версиях ядра СУБД Microsoft Jet инструкции SQL автоматически внедрялись в неявные транзакции.</span><span class="sxs-lookup"><span data-stu-id="407da-148">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions.</span></span> <span data-ttu-id="407da-149">Если часть выполненной инструкции с параметром **dbFailOnError** приводила к сбою, выполнялся откат всей инструкции.</span><span class="sxs-lookup"><span data-stu-id="407da-149">If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back.</span></span> <span data-ttu-id="407da-150">Для повышения производительности эти неявные транзакции были удалены начиная с версии 3.5.</span><span class="sxs-lookup"><span data-stu-id="407da-150">To improve performance, these implicit transactions were removed starting with version 3.5.</span></span> <span data-ttu-id="407da-151">При обновлении более ранних версий кода DAO рассмотрите возможность использования явных транзакций с инструкциями **Execute**.</span><span class="sxs-lookup"><span data-stu-id="407da-151">If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="407da-152">Чтобы добиться оптимальной производительности в рабочей области Microsoft Access, особенно в многопользовательской среде, вложите метод **Execute** в транзакцию.</span><span class="sxs-lookup"><span data-stu-id="407da-152">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction.</span></span> <span data-ttu-id="407da-153">Используйте метод **[BeginTrans](workspace-begintrans-method-dao.md)** для текущего объекта **[Workspace](workspace-object-dao.md)**, затем примените метод **Execute** и завершите транзакцию с помощью метода **[CommitTrans](workspace-committrans-method-dao.md)** для объекта **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="407da-153">Use the **[BeginTrans](workspace-begintrans-method-dao.md)** method on the current **[Workspace](workspace-object-dao.md)** object, then use the **Execute** method, and complete the transaction by using the **[CommitTrans](workspace-committrans-method-dao.md)** method on the **Workspace**.</span></span> <span data-ttu-id="407da-154">При этом изменения будут сохранены на диске, а все блокировки, установленные во время выполнения запроса, будут сняты.</span><span class="sxs-lookup"><span data-stu-id="407da-154">This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="407da-155">Пример</span><span class="sxs-lookup"><span data-stu-id="407da-155">Example</span></span>

<span data-ttu-id="407da-156">В этом примере показан метод **Execute**, запускаемый из объекта **QueryDef** и объекта **Database**.</span><span class="sxs-lookup"><span data-stu-id="407da-156">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object.</span></span> <span data-ttu-id="407da-157">Для запуска этой процедуры обязательно использовать процедуры ExecuteQueryDef и PrintOutput.</span><span class="sxs-lookup"><span data-stu-id="407da-157">The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

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

<span data-ttu-id="407da-158">В приведенном ниже примере показано, как выполнить запрос параметра.</span><span class="sxs-lookup"><span data-stu-id="407da-158">The following example shows how to execute a parameter query.</span></span> <span data-ttu-id="407da-159">Коллекция Parameters используется, чтобы задать параметр Organization запроса myActionQuery перед его выполнением.</span><span class="sxs-lookup"><span data-stu-id="407da-159">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="407da-160">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="407da-160">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
