---
title: Метод Recordset2.CancelUpdate (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13516830ddb9cb22e8e50872b51743ea5d54ab98
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921490"
---
# <a name="recordset2cancelupdate-method-dao"></a>Метод Recordset2.CancelUpdate (DAO)


**Применимо к**: Access 2013, Office 2013

Отменяет все ожидающие обновления для объекта **[набора записей](recordset-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . CancelUpdate (***UpdateType***)

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

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
<td><p>Установите одно из значений <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</p>

> [!NOTE]
> <P>Значения <EM>dbUpdateRegular</EM> и <EM>dbUpdateBatch</EM> являются допустимыми только в том случае, если обновление пакета включен.</P>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Чтобы отменить все ожидающие обновления, полученный после **[изменения](recordset2-edit-method-dao.md)** или **[AddNew](recordset2-addnew-method-dao.md)** операции можно использовать метод **CancelUpdate** . Например если пользователь вызывает метод **AddNew** или **Изменить** и еще не вызван метод **Update** , **CancelUpdate** показано, как отменить все изменения, внесенные после **изменения** или **AddNew** вызван.

Проверьте свойство **[EditMode](recordset2-editmode-property-dao.md)** **набора записей** для определения ожидающие операции, которая может быть отменена.


> [!NOTE]
> <P>С помощью метода <STRONG>CancelUpdate</STRONG> имеет тот же эффект, как перейти к другой записи без с помощью метода <STRONG><A href="recordset2-update-method-dao.md">Update</A></STRONG> , за исключением того, что текущей записи не изменяется и не обновляются различные свойства, такие как <STRONG><A href="recordset2-bof-property-dao.md">BOF</A></STRONG> и <STRONG><A href="recordset2-eof-property-dao.md">EOF</A></STRONG>.</P>



## <a name="example"></a>Пример

В этом примере показано использование метода **CancelUpdate** с помощью метода **AddNew** .

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

В этом примере показано, как метод **CancelUpdate** используется с методом **изменения** .

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

