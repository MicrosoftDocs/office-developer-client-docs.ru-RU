---
title: Метод Database.Execute (DAO)
TOCTitle: Execute method
ms:assetid: 9294d530-f70f-e1ed-3990-ce128de4378b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197654(v=office.15)
ms:contentKeyID: 48546378
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 5a2ebbb549e309349695d93618f4522a2dbf7a7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294962"
---
# <a name="databaseexecute-method-dao"></a><span data-ttu-id="35d0c-102">Метод Database.Execute (DAO)</span><span class="sxs-lookup"><span data-stu-id="35d0c-102">Database.Execute Method (DAO)</span></span>

<span data-ttu-id="35d0c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="35d0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35d0c-104">Выполняет запрос на изменение или запускает инструкцию SQL для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="35d0c-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d0c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35d0c-105">Syntax</span></span>

<span data-ttu-id="35d0c-106">*выражение* .Execute(***Query***, ***Options***)</span><span class="sxs-lookup"><span data-stu-id="35d0c-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="35d0c-107">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="35d0c-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="35d0c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="35d0c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35d0c-109">Имя</span><span class="sxs-lookup"><span data-stu-id="35d0c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="35d0c-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="35d0c-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="35d0c-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="35d0c-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="35d0c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="35d0c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35d0c-113"><em>Query</em></span><span class="sxs-lookup"><span data-stu-id="35d0c-113"><em>Query</em></span></span></p></td>
<td><p><span data-ttu-id="35d0c-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35d0c-114">Required</span></span></p></td>
<td><p><span data-ttu-id="35d0c-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="35d0c-115"><strong>String</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d0c-116"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="35d0c-116"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="35d0c-117">Необязательно</span><span class="sxs-lookup"><span data-stu-id="35d0c-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="35d0c-118"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="35d0c-118"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="35d0c-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="35d0c-119">Remarks</span></span>

<span data-ttu-id="35d0c-120">Можно использовать следующие константы **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** для параметров.</span><span class="sxs-lookup"><span data-stu-id="35d0c-120">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35d0c-121">Константа</span><span class="sxs-lookup"><span data-stu-id="35d0c-121">Constant</span></span></p></th>
<th><p><span data-ttu-id="35d0c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="35d0c-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35d0c-123"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="35d0c-123"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="35d0c-124">Отказывает в разрешении на запись другим пользователям (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="35d0c-124">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d0c-125"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="35d0c-125"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="35d0c-126">(По умолчанию) Выполняет несогласованные обновления (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="35d0c-126">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d0c-127"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="35d0c-127"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="35d0c-128">Выполняет согласованные обновления (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="35d0c-128">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d0c-129"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="35d0c-129"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="35d0c-130">Выполняет запрос SQL к серверу.</span><span class="sxs-lookup"><span data-stu-id="35d0c-130">Executes an SQL pass-through query.</span></span> <span data-ttu-id="35d0c-131">Установка этого параметра передает инструкцию SQL в базу данных ODBC для обработки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="35d0c-131">Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d0c-132"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="35d0c-132"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="35d0c-133">Выполняет откат обновлений, если возникает ошибка (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="35d0c-133">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d0c-134"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="35d0c-134"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="35d0c-135">Создает ошибку во время выполнения, если другой пользователь пытается изменить данные, которые вы редактируете (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="35d0c-135">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d0c-136"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="35d0c-136"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="35d0c-137">Выполняет запрос асинхронно (только для объектов ODBCDirect Connection и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="35d0c-137">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d0c-138"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="35d0c-138"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="35d0c-139">Выполняет инструкцию, не вызывая перед этим функцию API ODBC SQLPrepare (только для объектов ODBCDirect Connection и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="35d0c-139">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="35d0c-140">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="35d0c-140">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="35d0c-141">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="35d0c-141">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="35d0c-142">Константы **dbConsistent** и **dbInconsistent** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="35d0c-142">NOTE: The constants **dbConsistent** and **dbInconsistent** are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="35d0c-143">Можно использовать одну или другую, но не обе в заданном экземпляре **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="35d0c-143">You can use one or the other, but not both in a given instance of **OpenRecordset**.</span></span> <span data-ttu-id="35d0c-144">Одновременное использование **dbConsistent** и **dbInconsistent** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="35d0c-144">Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="35d0c-145">Метод **Execute** допустим только для запросов на изменение.</span><span class="sxs-lookup"><span data-stu-id="35d0c-145">The **Execute** method is valid only for action queries.</span></span> <span data-ttu-id="35d0c-146">Если вы используете метод **Execute** с другим типом запроса, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="35d0c-146">If you use **Execute** with another type of query, an error occurs.</span></span> <span data-ttu-id="35d0c-147">Так как запрос на изменение не возвращает записи, метод **Execute** не возвращает объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="35d0c-147">Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**.</span></span> <span data-ttu-id="35d0c-148">(Выполнение запроса SQL к серверу в рабочей области ODBCDirect не вызывает ошибку, если не возвращается объект **Recordset**.)</span><span class="sxs-lookup"><span data-stu-id="35d0c-148">(Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="35d0c-149">Свойство **RecordsAffected** объекта **Connection**, **Database** или **QueryDef** используется для определения числа записей, затронутых самым последним вызовом метода **Execute**.</span><span class="sxs-lookup"><span data-stu-id="35d0c-149">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method.</span></span> <span data-ttu-id="35d0c-150">Например, **RecordsAffected** содержит число записей, удаленных, обновленных или вставленных при выполнении запроса на изменение.</span><span class="sxs-lookup"><span data-stu-id="35d0c-150">For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query.</span></span> <span data-ttu-id="35d0c-151">Когда используется метод **Execute** для выполнения запроса, в качестве значения свойства **RecordsAffected** объекта **QueryDef** устанавливается число затронутых записей.</span><span class="sxs-lookup"><span data-stu-id="35d0c-151">When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="35d0c-152">Когда в рабочей области Microsoft Access указана синтаксически правильная инструкция SQL и имеются соответствующие разрешения, метод **Execute** не приводит к сбою, даже если не удается изменить или удалить ни одну строку.</span><span class="sxs-lookup"><span data-stu-id="35d0c-152">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted.</span></span> <span data-ttu-id="35d0c-153">Поэтому всегда используйте параметр **dbFailOnError** при применении метода **Execute** для выполнения обновления или удаления запроса.</span><span class="sxs-lookup"><span data-stu-id="35d0c-153">Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query.</span></span> <span data-ttu-id="35d0c-154">Этот параметр создает ошибку во время выполнения и откатывает все успешно выполненные изменения, если какие-либо затронутые записи заблокированы и не могут быть обновлены или удалены.</span><span class="sxs-lookup"><span data-stu-id="35d0c-154">This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="35d0c-155">В более ранних версиях ядра СУБД Microsoft Jet инструкции SQL автоматически внедрялись в неявные транзакции.</span><span class="sxs-lookup"><span data-stu-id="35d0c-155">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions.</span></span> <span data-ttu-id="35d0c-156">Если часть выполненной инструкции с параметром **dbFailOnError** приводила к сбою, выполнялся откат всей инструкции.</span><span class="sxs-lookup"><span data-stu-id="35d0c-156">If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back.</span></span> <span data-ttu-id="35d0c-157">Для повышения производительности эти неявные транзакции были удалены начиная с версии 3.5.</span><span class="sxs-lookup"><span data-stu-id="35d0c-157">To improve performance, these implicit transactions were removed starting with version 3.5.</span></span> <span data-ttu-id="35d0c-158">При обновлении более ранних версий кода DAO рассмотрите возможность использования явных транзакций с инструкциями **Execute**.</span><span class="sxs-lookup"><span data-stu-id="35d0c-158">If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="35d0c-159">Чтобы добиться оптимальной производительности в рабочей области Microsoft Access, особенно в многопользовательской среде, вложите метод **Execute** внутрь транзакции.</span><span class="sxs-lookup"><span data-stu-id="35d0c-159">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction.</span></span> <span data-ttu-id="35d0c-160">Используйте метод **BeginTrans** для текущего объекта **Workspace**, затем примените метод **Execute** и завершите транзакцию с помощью метода **CommitTrans** для объекта **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="35d0c-160">Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**.</span></span> <span data-ttu-id="35d0c-161">Это сохранит изменения на диске и освободит любые блокировки, установленные во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="35d0c-161">This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="35d0c-162">Пример</span><span class="sxs-lookup"><span data-stu-id="35d0c-162">Example</span></span>

<span data-ttu-id="35d0c-163">В этом примере показан метод **Execute**, запускаемый из объекта **QueryDef** и объекта **Database**.</span><span class="sxs-lookup"><span data-stu-id="35d0c-163">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object.</span></span> <span data-ttu-id="35d0c-164">Процедуры ExecuteQueryDef и PrintOutput являются обязательными для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="35d0c-164">The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

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
