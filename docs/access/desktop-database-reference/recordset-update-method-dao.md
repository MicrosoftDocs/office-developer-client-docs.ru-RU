---
title: Recordset.Update Method (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fa0b6897ea148a57cc17fcc0f908e2fdcae6b26
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480091"
---
# <a name="recordsetupdate-method-dao"></a><span data-ttu-id="3f3a5-102">Recordset.Update Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="3f3a5-102">Recordset.Update Method (DAO)</span></span>

<span data-ttu-id="3f3a5-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f3a5-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3a5-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f3a5-104">Syntax</span></span>

<span data-ttu-id="3f3a5-105">*выражение* . Обновление (***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="3f3a5-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="3f3a5-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="3f3a5-106">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="3f3a5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f3a5-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f3a5-108">Имя</span><span class="sxs-lookup"><span data-stu-id="3f3a5-108">Name</span></span></p></th>
<th><p><span data-ttu-id="3f3a5-109">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="3f3a5-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="3f3a5-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3f3a5-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="3f3a5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3f3a5-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f3a5-112">UpdateType</span><span class="sxs-lookup"><span data-stu-id="3f3a5-112">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="3f3a5-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="3f3a5-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="3f3a5-114"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="3f3a5-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="3f3a5-115"><strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> константу, указывающую тип обновления, как указано в настройки (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="3f3a5-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f3a5-116">Force</span><span class="sxs-lookup"><span data-stu-id="3f3a5-116">Force</span></span></p></td>
<td><p><span data-ttu-id="3f3a5-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="3f3a5-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="3f3a5-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="3f3a5-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="3f3a5-119"><strong>Логическое</strong> значение, указывающее ли принудительно изменения в базу данных, вне зависимости от ли данным был изменен другим пользователем <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Удалить</a></strong>, или <strong><a href="recordset-edit-method-dao.md">Изменение</a></strong> звонок.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-119">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset-edit-method-dao.md">Edit</a></strong> call.</span></span> <span data-ttu-id="3f3a5-120">Если <strong>значение True</strong>, принудительно изменений и изменения, внесенные другими пользователями, просто будут перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-120">If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten.</span></span> <span data-ttu-id="3f3a5-121">Если <strong>значение False</strong> (по умолчанию), изменения, внесенные другим пользователем до обновления будет отображено сбоя для эти изменения, которые находятся в конфликта обновления.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-121">If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict.</span></span> <span data-ttu-id="3f3a5-122">Ошибка не происходит, но свойства <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> и <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> будут указывать числа конфликтов и строк, затронутых конфликтов, соответственно (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="3f3a5-122">No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3f3a5-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="3f3a5-123">Remarks</span></span>

<span data-ttu-id="3f3a5-124">Для сохранения текущей записи и все изменения, внесенные в нее выполните **обновление** .</span><span class="sxs-lookup"><span data-stu-id="3f3a5-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f3a5-125">Изменения в текущей записи не сохраняются, если:</span><span class="sxs-lookup"><span data-stu-id="3f3a5-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="3f3a5-126">Используйте метод **AddNew** или **Изменить** и затем перетащить в другой записи без предварительного **обновления**.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="3f3a5-127">С помощью **AddNew**или **Изменить** и затем с помощью **изменения** или использованием **AddNew** еще раз без предварительного **обновления**.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="3f3a5-128">Присвойте свойству **[закладку](recordset-bookmark-property-dao.md)** к другой записи.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-128">You set the **[Bookmark](recordset-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="3f3a5-129">Закройте **записей** без предварительного **обновления**.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="3f3a5-130">Отменить операцию **редактирования** с помощью **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="3f3a5-131">Чтобы изменить запись, используйте метод **Изменить** чтобы скопировать содержимое текущей записи в буфер копирования.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-131">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer.</span></span> <span data-ttu-id="3f3a5-132">Если вы не используете **Изменение** сначала, возникает ошибка при использовании **обновления** или предпринята попытка изменить значение поля.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-132">If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="3f3a5-133">В рабочей области технология ODBCDirect, можно сделать пакета обновления, предоставляемые библиотека курсора поддерживает пакетные обновления и **записей** было открыто с помощью пакета оптимистичный блокировки параметр.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="3f3a5-134">В рабочей области Microsoft Access когда объекта **набора записей** **LockEdits** задается **значение True** (pessimistically заблокирован) в многопользовательской среде запись остается заблокированным с момента **Изменение** используется до \*\* Обновление\*\* метода или изменение отменяется.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="3f3a5-135">Если значение свойства **LockEdits** равно **False** (оптимистичном случае заблокирован), запись блокируется и по сравнению с предварительно измененной записи непосредственно перед обновляется в базе данных.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> 

<span data-ttu-id="3f3a5-136">Если запись была изменена используется метод **изменения** , происходит сбой операции **обновления** .</span><span class="sxs-lookup"><span data-stu-id="3f3a5-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="3f3a5-137">Базы данных Microsoft Access модуль подключения ODBC и устанавливаемый драйвер ISAM баз данных всегда использовать оптимистичный блокировки.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="3f3a5-138">Чтобы продолжить операцию **обновления** внесенными изменениями, используйте метод **обновления** еще раз.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="3f3a5-139">Вернуться к записи другого пользователя изменен, необходимо обновить текущей записи с помощью перемещения 0.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>


> [!NOTE]
> <span data-ttu-id="3f3a5-140">Чтобы добавить, изменить или удалить записи, должен существовать уникальный индекс на запись в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-140">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="3f3a5-141">Если нет, произойдет ошибка «Отказано в разрешении» на **AddNew**, **Удаление**или **Изменение** вызова метода в рабочей области Microsoft Access или приведет к возникновению ошибки «Недопустимый аргумент» при вызове **Update** в рабочей области технология ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-141">If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>

## <a name="example"></a><span data-ttu-id="3f3a5-142">Пример</span><span class="sxs-lookup"><span data-stu-id="3f3a5-142">Example</span></span>

<span data-ttu-id="3f3a5-143">В этом примере демонстрируется метод **Update** в сочетании с помощью метода **Edit** .</span><span class="sxs-lookup"><span data-stu-id="3f3a5-143">This example demonstrates the **Update** method in conjunction with **Edit** method.</span></span>

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

<span data-ttu-id="3f3a5-144">В этом примере демонстрируется использование метода **обновления** в сочетании с помощью метода **AddNew** .</span><span class="sxs-lookup"><span data-stu-id="3f3a5-144">This example demonstrates the **Update** method in conjunction with the **AddNew** method.</span></span>

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

<span data-ttu-id="3f3a5-145">В этом примере используется свойство **BatchCollisionCount** и метод **Update** для демонстрации пакетного обновления, где разрешены все конфликты с помощью принудительной пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-145">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

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

<span data-ttu-id="3f3a5-146">В этом примере используется метод **AddNew** , чтобы создать новую запись с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-146">This example uses the **AddNew** method to create a new record with the specified name.</span></span> <span data-ttu-id="3f3a5-147">Функция AddName является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-147">The AddName function is required for this procedure to run.</span></span>

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
