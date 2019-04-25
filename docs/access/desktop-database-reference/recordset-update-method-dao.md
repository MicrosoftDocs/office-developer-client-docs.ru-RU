---
title: Метод Recordset.Update (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 9f73dfc49a6ec99b726a052c588c032783010081
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307527"
---
# <a name="recordsetupdate-method-dao"></a><span data-ttu-id="8a6be-102">Метод Recordset.Update (DAO)</span><span class="sxs-lookup"><span data-stu-id="8a6be-102">Recordset.Update method (DAO)</span></span>

<span data-ttu-id="8a6be-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a6be-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6be-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a6be-104">Syntax</span></span>

<span data-ttu-id="8a6be-105">*expression* .Update(***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="8a6be-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="8a6be-106">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="8a6be-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a6be-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a6be-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a6be-108">Имя</span><span class="sxs-lookup"><span data-stu-id="8a6be-108">Name</span></span></p></th>
<th><p><span data-ttu-id="8a6be-109">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="8a6be-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="8a6be-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8a6be-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="8a6be-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8a6be-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a6be-112"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="8a6be-112"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="8a6be-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="8a6be-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="8a6be-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="8a6be-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6be-115">Константа <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong>, обозначающая тип обновления, заданный в параметрах (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8a6be-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a6be-116"><em>Сила</em></span><span class="sxs-lookup"><span data-stu-id="8a6be-116"><em>Force</em></span></span></p></td>
<td><p><span data-ttu-id="8a6be-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="8a6be-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="8a6be-118"><strong>Логический</strong></span><span class="sxs-lookup"><span data-stu-id="8a6be-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6be-119"><strong>Логическое</strong> значение, указывающее, следует ли принудительно вносить изменения в базу данных независимо от того, были ли базовые данные изменены другим пользователем с момента вызова метода <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> или <strong><a href="recordset-edit-method-dao.md">Edit</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="8a6be-119">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset-edit-method-dao.md">Edit</a></strong> call.</span></span> <span data-ttu-id="8a6be-120">Если задано значение <strong>True</strong>, то ваши изменения принудительно применяются, а изменения, внесенные другими пользователями, просто перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="8a6be-120">If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten.</span></span> <span data-ttu-id="8a6be-121">Если задано значение <strong>False</strong> (по умолчанию), то изменения, внесенные другими пользователями, пока обновление ожидает обработки, приведут к сбоям обновления в конфликтных участках.</span><span class="sxs-lookup"><span data-stu-id="8a6be-121">If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict.</span></span> <span data-ttu-id="8a6be-122">Ошибка не возникает, но в свойствах <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> и <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> указывается количество конфликтов и затронутых ими строк, соответственно (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8a6be-122">No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8a6be-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a6be-123">Remarks</span></span>

<span data-ttu-id="8a6be-124">Используйте метод **Update**, чтобы сохранить текущую запись и все внесенные в нее изменения.</span><span class="sxs-lookup"><span data-stu-id="8a6be-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a6be-125">Изменения текущей записи теряются, если:</span><span class="sxs-lookup"><span data-stu-id="8a6be-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="8a6be-126">вызвать метод **Edit** или **AddNew**, а затем перейти к другой записи, не используя перед этим метод **Update**;</span><span class="sxs-lookup"><span data-stu-id="8a6be-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="8a6be-127">вызвать метод **Edit** или **AddNew**, а затем снова применить метод **Edit** или **AddNew**, не используя перед этим метод **Update**;</span><span class="sxs-lookup"><span data-stu-id="8a6be-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="8a6be-128">указать в свойстве **[Bookmark](recordset-bookmark-property-dao.md)** другую запись;</span><span class="sxs-lookup"><span data-stu-id="8a6be-128">You set the **[Bookmark](recordset-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="8a6be-129">закрыть объект **Recordset**, не используя перед этим метод **Update**;</span><span class="sxs-lookup"><span data-stu-id="8a6be-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="8a6be-130">отменить операцию **Edit** с помощью метода **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8a6be-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="8a6be-131">Чтобы изменить запись, используйте метод **Edit** для копирования содержимого текущей записи в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="8a6be-131">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer.</span></span> <span data-ttu-id="8a6be-132">Если сначала не вызвать метод **Edit**, то при использовании метода **Update** или попытке изменить значение поля возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="8a6be-132">If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="8a6be-133">В рабочей области ODBCDirect можно выполнять пакетное обновление, при условии что библиотека курсоров поддерживает его, а объект **Recordset** был открыт с использованием оптимистичной блокировки пакетных операций.</span><span class="sxs-lookup"><span data-stu-id="8a6be-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="8a6be-134">Если в рабочей области Microsoft Access для свойства **LockEdits** объекта **Recordset** задано значение **True** (пессимистичная блокировка) в многопользовательской среде, то запись останется заблокированной с момента вызова метода **Edit** до завершения выполнения метода **Update** или отмены изменения.</span><span class="sxs-lookup"><span data-stu-id="8a6be-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="8a6be-135">Если для свойства **LockEdits** задано значение **False** (оптимистичная блокировка), то запись блокируется и сравнивается с ее вариантом непосредственно перед обновлением в базе данных.</span><span class="sxs-lookup"><span data-stu-id="8a6be-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> 

<span data-ttu-id="8a6be-136">Если запись изменилась с момента использования метода **Edit**, происходит сбой операции **Update**.</span><span class="sxs-lookup"><span data-stu-id="8a6be-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="8a6be-137">В базах данных ODBC, подключенных к ядру СУБД Microsoft Access, и устанавливаемых базах данных ISAM всегда используется оптимистичная блокировка.</span><span class="sxs-lookup"><span data-stu-id="8a6be-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="8a6be-138">Чтобы продолжить выполнение операции **Update** с вашими изменениями, снова вызовите метод **Update**.</span><span class="sxs-lookup"><span data-stu-id="8a6be-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="8a6be-139">Чтобы вернуть запись в состояние, оставленное другим пользователем, обновите текущую запись с помощью команды Move 0.</span><span class="sxs-lookup"><span data-stu-id="8a6be-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>

> [!NOTE]
> <span data-ttu-id="8a6be-140">Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс.</span><span class="sxs-lookup"><span data-stu-id="8a6be-140">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="8a6be-141">В противном случае возникнет ошибка "Отказано в разрешении" (при вызове метода **AddNew**, **Delete** или **Edit** в рабочей области Microsoft Access) или ошибка "Недопустимый аргумент" (при вызове метода **Update** в рабочей области ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8a6be-141">If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>

## <a name="example"></a><span data-ttu-id="8a6be-142">Пример</span><span class="sxs-lookup"><span data-stu-id="8a6be-142">Example</span></span>

<span data-ttu-id="8a6be-143">В этом примере показано использование метода **Update** вместе с методом **Edit**.</span><span class="sxs-lookup"><span data-stu-id="8a6be-143">This example demonstrates the **Update** method in conjunction with **Edit** method.</span></span>

```vb
    Sub UpdateX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .Edit 
     ' Store original data. 
     strOldFirst = !FirstName 
     strOldLast = !LastName 
     ' Change data in edit buffer. 
     !FirstName = "Linda" 
     !LastName = "Kobara" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "Edit in progress:" & vbCr & _ 
     " Original data = " & strOldFirst & " " & _ 
     strOldLast & vbCr & " Data in buffer = " & _ 
     !FirstName & " " & !LastName & vbCr & vbCr & _ 
     "Use Update to replace the original data with " & _ 
     "the buffered data in the Recordset?" 
     
     If MsgBox(strMessage, vbYesNo) = vbYes Then 
     .Update 
     Else 
     .CancelUpdate 
     End If 
     
     ' Show the resulting data. 
     MsgBox "Data in recordset = " & !FirstName & " " & _ 
     !LastName 
     
     ' Restore original data because this is a demonstration. 
     If Not (strOldFirst = !FirstName And _ 
     strOldLast = !LastName) Then 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="8a6be-144">В этом примере показано использование метода **Update** вместе с методом **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="8a6be-144">This example demonstrates the **Update** method in conjunction with the **AddNew** method.</span></span>

```vb
    Sub UpdateX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .AddNew 
     !FirstName = "Bill" 
     !LastName = "Sornsin" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "AddNew in progress:" & vbCr & _ 
     " Data in buffer = " & !FirstName & " " & _ 
     !LastName & vbCr & vbCr & _ 
     "Use Update to save buffer to recordset?" 
     
     If MsgBox(strMessage, vbYesNoCancel) = vbYes Then 
     .Update 
     ' Go to the new record and show the resulting data. 
     .Bookmark = .LastModified 
     MsgBox "Data in recordset = " & !FirstName & _ 
     " " & !LastName 
     ' Delete new data because this is a demonstration. 
     .Delete 
     Else 
     .CancelUpdate 
     MsgBox "No new record added." 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="8a6be-145">В этом примере используются свойство **BatchCollisionCount** и метод **Update**, чтобы продемонстрировать пакетное обновление с разрешением всех конфликтов путем принудительного пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="8a6be-145">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="8a6be-146">В этом примере используется метод **AddNew**, чтобы создать запись с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="8a6be-146">This example uses the **AddNew** method to create a new record with the specified name.</span></span> <span data-ttu-id="8a6be-147">Функция AddName необходима для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="8a6be-147">The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
