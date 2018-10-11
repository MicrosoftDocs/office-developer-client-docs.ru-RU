---
title: Recordset.Move Method (DAO)
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
ms.openlocfilehash: 23de94392fb2d9f1b0106c39f21a8872783b6d7b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482183"
---
# <a name="recordsetmove-method-dao"></a>Recordset.Move Method (DAO)


**Применимо к**: Access 2013 | Office 2013

Перемещает положение текущей записи в объекте **[набора записей](recordset-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . Перемещение (***строк***, ***StartBookmark***)

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
<td><p>Строки</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Длинный</strong></p></td>
<td><p>Количество строк, которые будут перемещаться положение. Если строк больше 0, положение перемещается вперед (ближе к концу файла). Если строк меньше 0, положение перемещается назад (к началу файла).</p></td>
</tr>
<tr class="even">
<td><p>StartBookmark</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Значение, идентифицирующее закладку. При указании startbookmark move начинается относительно эту закладку. В противном случае перемещение начинается с текущей записи.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Если вы используете **Перемещение** навести указатель текущей записи перед первой записи указатель текущей записи перемещает в начало файла. Если **записей** не содержит записей и его свойство **[BOF](recordset-bof-property-dao.md)** имеет **значение True**, с помощью этого метода для перемещения назад приводит к ошибке.

Если вы можете **переместить** наведите указатель текущей записи после последней записи, текущей позиции указателя записи перемещается в конец файла. Если **записей** не содержит записей и его свойство **[EOF](recordset-eof-property-dao.md)** имеет **значение True**, затем перейти вперед, с помощью этого метода приводит к ошибке.

Если параметр **BOF** или **EOF** свойство имеет **значение True** , и попытаться использовать метод **Move** без допустимого закладку, возникает ошибка времени выполнения.


> [!NOTE]
> <UL>
> <LI>
> <P>При использовании <STRONG>Перемещение</STRONG> на объект <STRONG>набора записей</STRONG> прямого только для типа аргумент строки должно быть положительное целое число, и закладки не разрешается. Это означает, что можно только Переместить вперед.</P>
> <LI>
> <P>Чтобы сделать первый, и, наконец, следующий или предыдущий записи в <STRONG>набор записей</STRONG> текущей записи метод <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG>или <STRONG>MovePrevious</STRONG> .</P>
> <LI>
> <P>Использование <STRONG>Перемещение</STRONG> с строк равно 0 — это простой способ получения данных для текущей записи. Эта функция особенно полезна, если вы хотите убедиться, что текущая запись имеет самых последних данных из базовых таблиц. Он также будет отменить все ожидающие <STRONG><A href="recordset2-edit-method-dao.md">изменения</A></STRONG> или <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> вызовы.</P></LI></UL>



## <a name="example"></a>Пример

В этом примере используется метод **Move** навести указатель записи, в зависимости от введенных пользователем.

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
