---
title: Метод Recordset2. Move (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d57e73c52ca515f13d613ed3aeb9cf361054396e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307268"
---
# <a name="recordset2move-method-dao"></a>Метод Recordset2. Move (DAO)

**Область применения**: Access 2013, Office 2013

Перемещает положение текущей записью в объекте **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*Expression* . Move (***Rows***, ***стартбукмарк***)

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

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
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Rows</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Число строк, которое будет перемещено в позицию. Если число строк больше 0, положение перемещается вперед (ближе к концу файла). Если число строк меньше 0, положение перемещается назад (к началу файла).</p></td>
</tr>
<tr class="even">
<td><p><em>Стартбукмарк</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Значение, определяющее закладку. При указании стартбукмарк перемещение начинается относительно этой закладки. В противном случае перемещение начинается с текущей записи.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Если вы используете **Move** для размещения указателя текущей записи перед первой записью, указатель текущей записи перемещается в начало файла. Если объект **Recordset** не содержит записей и его свойство **[BOF](recordset2-bof-property-dao.md)** имеет **значение true**, использование этого метода для перемещения назад приводит к ошибке.

Если вы используете **Move** , чтобы переместить указатель текущей записи после последней записи, положение указателя текущей записи перемещается в конец файла. Если **набор записей** не содержит записей и свойство **[EOF](recordset2-eof-property-dao.md)** имеет **значение true**, то при использовании этого метода для перемещения вперед возникает ошибка.

Если свойство **BOF** или **EOF** имеет **значение true** и вы пытаетесь использовать метод **Move** без допустимой закладки, возникает ошибка времени выполнения.

> [!NOTE]
> - Если вы используете **Move** для объекта **Recordset** с типом "вперед", аргумент Rows должен быть положительным целым числом, а закладки не разрешены. Это означает, что вы можете перемещаться только вперед.
> - Чтобы сделать первую, последнюю, следующую или предыдущую запись в наборе **записей** текущей записи, используйте метод **MoveFirst**, **MoveLast**, **MoveNext**или **MovePrevious** .
> - Использование **Move** со строками, равными 0 — это простой способ получить базовые данные для текущей записи. Это полезно, если необходимо убедиться, что текущая запись содержит самые последние данные из базовых таблиц. Кроме того, он отменяет все ожидающие вызовы **[Edit](recordset2-edit-method-dao.md)** или **[AddNew](recordset-addnew-method-dao.md)** .


## <a name="example"></a>Пример

В этом примере с помощью метода **Move** замещается указатель записи на основании вводимых пользователем данных.

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset2 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
