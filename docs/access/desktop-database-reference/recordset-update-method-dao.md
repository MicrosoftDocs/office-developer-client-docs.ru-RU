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
# <a name="recordsetupdate-method-dao"></a>Метод Recordset.Update (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*expression* .Update(***UpdateType***, ***Force***)

*expression*: переменная, представляющая объект **Recordset**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Константа <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong>, обозначающая тип обновления, заданный в параметрах (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><em>Сила</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Логический</strong></p></td>
<td><p><strong>Логическое</strong> значение, указывающее, следует ли принудительно вносить изменения в базу данных независимо от того, были ли базовые данные изменены другим пользователем с момента вызова метода <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> или <strong><a href="recordset-edit-method-dao.md">Edit</a></strong>. Если задано значение <strong>True</strong>, то ваши изменения принудительно применяются, а изменения, внесенные другими пользователями, просто перезаписываются. Если задано значение <strong>False</strong> (по умолчанию), то изменения, внесенные другими пользователями, пока обновление ожидает обработки, приведут к сбоям обновления в конфликтных участках. Ошибка не возникает, но в свойствах <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> и <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> указывается количество конфликтов и затронутых ими строк, соответственно (только для рабочих областей ODBCDirect).</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Используйте метод **Update**, чтобы сохранить текущую запись и все внесенные в нее изменения.

> [!IMPORTANT]
> Изменения текущей записи теряются, если:
> - вызвать метод **Edit** или **AddNew**, а затем перейти к другой записи, не используя перед этим метод **Update**;
> - вызвать метод **Edit** или **AddNew**, а затем снова применить метод **Edit** или **AddNew**, не используя перед этим метод **Update**;
> - указать в свойстве **[Bookmark](recordset-bookmark-property-dao.md)** другую запись;
> - закрыть объект **Recordset**, не используя перед этим метод **Update**;
> - отменить операцию **Edit** с помощью метода **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

Чтобы изменить запись, используйте метод **Edit** для копирования содержимого текущей записи в буфер обмена. Если сначала не вызвать метод **Edit**, то при использовании метода **Update** или попытке изменить значение поля возникнет ошибка.

В рабочей области ODBCDirect можно выполнять пакетное обновление, при условии что библиотека курсоров поддерживает его, а объект **Recordset** был открыт с использованием оптимистичной блокировки пакетных операций.

Если в рабочей области Microsoft Access для свойства **LockEdits** объекта **Recordset** задано значение **True** (пессимистичная блокировка) в многопользовательской среде, то запись останется заблокированной с момента вызова метода **Edit** до завершения выполнения метода **Update** или отмены изменения. Если для свойства **LockEdits** задано значение **False** (оптимистичная блокировка), то запись блокируется и сравнивается с ее вариантом непосредственно перед обновлением в базе данных. 

Если запись изменилась с момента использования метода **Edit**, происходит сбой операции **Update**. В базах данных ODBC, подключенных к ядру СУБД Microsoft Access, и устанавливаемых базах данных ISAM всегда используется оптимистичная блокировка. Чтобы продолжить выполнение операции **Update** с вашими изменениями, снова вызовите метод **Update**. Чтобы вернуть запись в состояние, оставленное другим пользователем, обновите текущую запись с помощью команды Move 0.

> [!NOTE]
> Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс. В противном случае возникнет ошибка "Отказано в разрешении" (при вызове метода **AddNew**, **Delete** или **Edit** в рабочей области Microsoft Access) или ошибка "Недопустимый аргумент" (при вызове метода **Update** в рабочей области ODBCDirect).

## <a name="example"></a>Пример

В этом примере показано использование метода **Update** вместе с методом **Edit**.

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

В этом примере показано использование метода **Update** вместе с методом **AddNew**.

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

В этом примере используются свойство **BatchCollisionCount** и метод **Update**, чтобы продемонстрировать пакетное обновление с разрешением всех конфликтов путем принудительного пакетного обновления.

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

В этом примере используется метод **AddNew**, чтобы создать запись с указанным именем. Функция AddName необходима для запуска этой процедуры.

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
