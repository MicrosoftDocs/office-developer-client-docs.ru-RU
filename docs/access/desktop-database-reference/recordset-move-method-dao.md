---
title: Метод Recordset.Move (DAO)
TOCTitle: Move Method
ms:assetid: 21ca5ab5-ff71-1ae8-21b3-8991d5f795cf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191697(v=office.15)
ms:contentKeyID: 48543689
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052941
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1f10b5b779141189f114e420b3f7d4827e701161
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284801"
---
# <a name="recordsetmove-method-dao"></a>Метод Recordset.Move (DAO)

**Область применения**: Access 2013, Office 2013

Перемещает положение текущей записи в объекте **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*expression* .Move(***Rows***, ***StartBookmark***)

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
<td><p><em>Rows</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Количество строк, на которое сдвинется положение. Если значение rows больше 0, то положение смещается вперед (к концу файла). Если оно меньше 0, то положение смещается назад (к началу файла).</p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Значение, определяющее закладку. Если указать значение startbookmark, смещение начнется относительно закладки. В противном случае оно начнется с текущей записи.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Если с помощью метода **Move** поместить указатель текущей записи перед первой записью, то указатель текущей записи переместится в начало файла. Если объект **Recordset** не содержит записей, а для его свойства **[BOF](recordset-bof-property-dao.md)** задано значение **True**, то при попытке использовать этот метод для перемещения назад возникнет ошибка.

Если с помощью метода **Move** поместить указатель текущей записи после последней записи, то указатель текущей записи переместится в конец файла. Если объект **Recordset** не содержит записей, а для его свойства **[EOF](recordset-eof-property-dao.md)** задано значение **True**, то при попытке использовать этот метод для перемещения вперед возникнет ошибка.

Если для свойства **BOF** или **EOF** задано значение **True**, а вы попытаетесь использовать метод **Move** без действительной закладки, возникнет ошибка во время выполнения.

> [!NOTE]
> - Если использовать метод **Move** для однонаправленного объекта **Recordset**, значение аргумента rows должно быть положительным целым числом, а использование закладок не допускается. Это означает, что перемещать запись можно только вперед.
> - Чтобы сделать первую, последнюю, следующую или предыдущую запись в объекте **Recordset** текущей, используйте метод **MoveFirst**, **MoveLast**, **MoveNext** или **MovePrevious**.
> - Используя метод **Move** и задав для аргумента rows значение 0, можно легко получить базовые данные для текущей записи. Это полезно, если вы хотите убедиться, что текущая запись содержит наиболее актуальные данные из базовых таблиц. При этом также будут отменены все ожидающие обработки вызовы методов **[Edit](recordset2-edit-method-dao.md)** и **[AddNew](recordset-addnew-method-dao.md)**.


## <a name="example"></a>Пример

В этом примере с помощью метода **Move** указатель перемещается в соответствии с вводимыми пользователем данными.

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset 
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
