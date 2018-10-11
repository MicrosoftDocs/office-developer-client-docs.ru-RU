---
title: Database.Execute Method (DAO)
TOCTitle: Execute Method
ms:assetid: 9294d530-f70f-e1ed-3990-ce128de4378b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197654(v=office.15)
ms:contentKeyID: 48546378
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1c66e6d3297359b3f3584932d8a1faa5dbee0fd7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480256"
---
# <a name="databaseexecute-method-dao"></a><span data-ttu-id="25db1-102">Database.Execute Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="25db1-102">Database.Execute Method (DAO)</span></span>

<span data-ttu-id="25db1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="25db1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="25db1-104">Запуск запроса или выполняет инструкции SQL на указанный объект.</span><span class="sxs-lookup"><span data-stu-id="25db1-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="25db1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25db1-105">Syntax</span></span>

<span data-ttu-id="25db1-106">*выражение* . Выполнение (***запроса***, ***Параметры***)</span><span class="sxs-lookup"><span data-stu-id="25db1-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="25db1-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="25db1-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="25db1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="25db1-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25db1-109">Имя</span><span class="sxs-lookup"><span data-stu-id="25db1-109">Name</span></span></p></th>
<th><p><span data-ttu-id="25db1-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="25db1-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="25db1-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="25db1-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="25db1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="25db1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25db1-113">Query</span><span class="sxs-lookup"><span data-stu-id="25db1-113">Query</span></span></p></td>
<td><p><span data-ttu-id="25db1-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="25db1-114">Required</span></span></p></td>
<td><p><span data-ttu-id="25db1-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="25db1-115"><strong>String</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25db1-116">Options</span><span class="sxs-lookup"><span data-stu-id="25db1-116">Options</span></span></p></td>
<td><p><span data-ttu-id="25db1-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="25db1-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="25db1-118"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="25db1-118"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="25db1-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="25db1-119">Remarks</span></span>

<span data-ttu-id="25db1-120">Следующие константы **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** можно использовать для доступа к параметрам.</span><span class="sxs-lookup"><span data-stu-id="25db1-120">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25db1-121">Константа</span><span class="sxs-lookup"><span data-stu-id="25db1-121">Constant</span></span></p></th>
<th><p><span data-ttu-id="25db1-122">Описание</span><span class="sxs-lookup"><span data-stu-id="25db1-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25db1-123"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="25db1-123"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="25db1-124">Запрещает разрешение на запись другим пользователям (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="25db1-124">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25db1-125"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="25db1-125"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="25db1-126">(По умолчанию) Выполняет несогласованных обновлений (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="25db1-126">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25db1-127"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="25db1-127"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="25db1-128">Выполняет согласованности обновлений (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="25db1-128">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25db1-129"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="25db1-129"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="25db1-130">Выполняет запрос к серверу.</span><span class="sxs-lookup"><span data-stu-id="25db1-130">Executes an SQL pass-through query.</span></span> <span data-ttu-id="25db1-131">Если этот параметр передает инструкции SQL к базе данных ODBC для обработки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="25db1-131">Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25db1-132"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="25db1-132"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="25db1-133">Откат обновления при возникновении ошибки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="25db1-133">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25db1-134"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="25db1-134"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="25db1-135">Создает ошибку времени выполнения, если другой пользователь изменение данных, редактировании (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="25db1-135">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25db1-136"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="25db1-136"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="25db1-137">Выполняет асинхронный запрос (только объекты технология ODBCDirect подключения и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="25db1-137">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25db1-138"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="25db1-138"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="25db1-139">Выполняет оператор без первого вызова функции SQLPrepare ODBC API (только объекты технология ODBCDirect подключения и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="25db1-139">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="25db1-140">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="25db1-140">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="25db1-141">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="25db1-141">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="25db1-142">Константы **dbConsistent** и **dbInconsistent** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="25db1-142">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive.</span></span> <span data-ttu-id="25db1-143">Можно использовать одно или другое, но не оба в экземпляре **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="25db1-143">You can use one or the other, but not both in a given instance of **OpenRecordset**.</span></span> <span data-ttu-id="25db1-144">С помощью **dbConsistent** и **dbInconsistent** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="25db1-144">Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="25db1-145">Метод **Execute** действителен только для запросов.</span><span class="sxs-lookup"><span data-stu-id="25db1-145">The **Execute** method is valid only for action queries.</span></span> <span data-ttu-id="25db1-146">Если вы используете **Execute** с запрос другого типа, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="25db1-146">If you use **Execute** with another type of query, an error occurs.</span></span> <span data-ttu-id="25db1-147">Поскольку запрос не возвращает все записи, **выполнение** не возвращает **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="25db1-147">Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**.</span></span> <span data-ttu-id="25db1-148">(Выполнение запроса к серверу в рабочей области технология ODBCDirect не возвращает ошибку при **записей** не возвращаются.)</span><span class="sxs-lookup"><span data-stu-id="25db1-148">(Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="25db1-149">Используйте свойство **RecordsAffected** объекта **подключения**, **базы данных**или **QueryDef** для определения количества записей, влияет на последнюю метод **Execute** .</span><span class="sxs-lookup"><span data-stu-id="25db1-149">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method.</span></span> <span data-ttu-id="25db1-150">Например **RecordsAffected** содержит число записей удален, обновляется или вставляется при выполнении запроса.</span><span class="sxs-lookup"><span data-stu-id="25db1-150">For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query.</span></span> <span data-ttu-id="25db1-151">При использовании метода **Execute** для выполнения запроса, свойство **RecordsAffected** объекта **QueryDef** присваивается количество записей.</span><span class="sxs-lookup"><span data-stu-id="25db1-151">When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="25db1-152">В рабочей области Microsoft Access, если предоставить синтаксически правильные инструкции SQL и имеют соответствующие разрешения метода **Execute** не ошибка — даже в том случае, если не одной строки можно изменить или удалить.</span><span class="sxs-lookup"><span data-stu-id="25db1-152">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted.</span></span> <span data-ttu-id="25db1-153">Таким образом всегда используйте параметр **dbFailOnError** , при использовании метода **Execute** для запуска и обновления или удаления запроса.</span><span class="sxs-lookup"><span data-stu-id="25db1-153">Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query.</span></span> <span data-ttu-id="25db1-154">Этот параметр, возникает ошибка времени выполнения и выполняет откат всех изменений успешно Если никакой из записей влияет на блокируется и не может быть обновлении или удалении.</span><span class="sxs-lookup"><span data-stu-id="25db1-154">This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="25db1-155">В более ранних версиях ядра базы данных Microsoft Jet SQL операторы автоматически были внедрены в неявные транзакции.</span><span class="sxs-lookup"><span data-stu-id="25db1-155">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions.</span></span> <span data-ttu-id="25db1-156">Если не удалось выполнить инструкции, с **dbFailOnError** , всей оператор будет выполнен откат.</span><span class="sxs-lookup"><span data-stu-id="25db1-156">If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back.</span></span> <span data-ttu-id="25db1-157">В целях повышения производительности эти неявные транзакции были удалены, начиная с версии 3.5.</span><span class="sxs-lookup"><span data-stu-id="25db1-157">To improve performance, these implicit transactions were removed starting with version 3.5.</span></span> <span data-ttu-id="25db1-158">При обновлении старых кода DAO, необходимо принять во внимание использование явных транзакций вокруг **выполнение** инструкций.</span><span class="sxs-lookup"><span data-stu-id="25db1-158">If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="25db1-159">Для достижения наилучшей производительности в рабочую область для Microsoft Access, особенно в многопользовательской среде вложить метода **Execute** внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="25db1-159">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction.</span></span> <span data-ttu-id="25db1-160">Используйте метод **BeginTrans** на текущий объект **рабочей области** , а затем используйте метод **Execute** и завершения транзакции с помощью метода **CommitTrans** в **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="25db1-160">Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**.</span></span> <span data-ttu-id="25db1-161">Это сохраняет изменения на диске и освобождает любые блокировки во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="25db1-161">This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="25db1-162">Пример</span><span class="sxs-lookup"><span data-stu-id="25db1-162">Example</span></span>

<span data-ttu-id="25db1-163">В этом примере демонстрируется использование метода **Execute** при вызове из объекта **QueryDef** и объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="25db1-163">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object.</span></span> <span data-ttu-id="25db1-164">Процедуры ExecuteQueryDef и PrintOutput необходимы для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="25db1-164">The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

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
     Debug.Print " " & rstTemp!LastName & _ 
     ", " & rstTemp!Country 
     rstTemp.MoveNext 
     Loop 
     
    End Sub
```
