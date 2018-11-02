---
title: Метод Recordset.Update (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d095fd8288ddd3b778bb8d4384fdea9e423ad8d1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930310"
---
# <a name="recordsetupdate-method-dao"></a>Метод Recordset.Update (DAO)

**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . Обновление (***UpdateType***, ***Force***)

*выражение* Переменная, которая представляет собой объект **набора записей** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>UpdateType</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Длинный</strong></p></td>
<td><p><strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> константу, указывающую тип обновления, как указано в настройки (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p>Force</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p><strong>Логическое</strong> значение, указывающее ли принудительно изменения в базу данных, вне зависимости от ли данным был изменен другим пользователем <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Удалить</a></strong>, или <strong><a href="recordset-edit-method-dao.md">Изменение</a></strong> звонок. Если <strong>значение True</strong>, принудительно изменений и изменения, внесенные другими пользователями, просто будут перезаписаны. Если <strong>значение False</strong> (по умолчанию), изменения, внесенные другим пользователем до обновления будет отображено сбоя для эти изменения, которые находятся в конфликта обновления. Ошибка не происходит, но свойства <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> и <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> будут указывать числа конфликтов и строк, затронутых конфликтов, соответственно (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Для сохранения текущей записи и все изменения, внесенные в нее выполните **обновление** .

> [!IMPORTANT]
> Изменения в текущей записи не сохраняются, если:
> - Используйте метод **AddNew** или **Изменить** и затем перетащить в другой записи без предварительного **обновления**.
> - С помощью **AddNew**или **Изменить** и затем с помощью **изменения** или использованием **AddNew** еще раз без предварительного **обновления**.
> - Присвойте свойству **[закладку](recordset-bookmark-property-dao.md)** к другой записи.
> - Закройте **записей** без предварительного **обновления**.
> - Отменить операцию **редактирования** с помощью **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

Чтобы изменить запись, используйте метод **Изменить** чтобы скопировать содержимое текущей записи в буфер копирования. Если вы не используете **Изменение** сначала, возникает ошибка при использовании **обновления** или предпринята попытка изменить значение поля.

В рабочей области технология ODBCDirect, можно сделать пакета обновления, предоставляемые библиотека курсора поддерживает пакетные обновления и **записей** было открыто с помощью пакета оптимистичный блокировки параметр.

В рабочей области Microsoft Access когда объекта **набора записей** **LockEdits** задается **значение True** (pessimistically заблокирован) в многопользовательской среде запись остается заблокированным с момента **Изменение** используется до ** Обновление** метода или изменение отменяется. Если значение свойства **LockEdits** равно **False** (оптимистичном случае заблокирован), запись блокируется и по сравнению с предварительно измененной записи непосредственно перед обновляется в базе данных. 

Если запись была изменена используется метод **изменения** , происходит сбой операции **обновления** . Базы данных Microsoft Access модуль подключения ODBC и устанавливаемый драйвер ISAM баз данных всегда использовать оптимистичный блокировки. Чтобы продолжить операцию **обновления** внесенными изменениями, используйте метод **обновления** еще раз. Вернуться к записи другого пользователя изменен, необходимо обновить текущей записи с помощью перемещения 0.


> [!NOTE]
> Чтобы добавить, изменить или удалить записи, должен существовать уникальный индекс на запись в источнике данных. Если нет, произойдет ошибка «Отказано в разрешении» на **AddNew**, **Удаление**или **Изменение** вызова метода в рабочей области Microsoft Access или приведет к возникновению ошибки «Недопустимый аргумент» при вызове **Update** в рабочей области технология ODBCDirect.

## <a name="example"></a>Пример

В этом примере демонстрируется метод **Update** в сочетании с помощью метода **Edit** .

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

В этом примере демонстрируется использование метода **обновления** в сочетании с помощью метода **AddNew** .

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

В этом примере используется свойство **BatchCollisionCount** и метод **Update** для демонстрации пакетного обновления, где разрешены все конфликты с помощью принудительной пакетного обновления.

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

В этом примере используется метод **AddNew** , чтобы создать новую запись с указанным именем. Функция AddName является обязательным для выполнения этой процедуры.

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
