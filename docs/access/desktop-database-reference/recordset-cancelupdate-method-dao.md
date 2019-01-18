---
title: Метод Recordset.CancelUpdate (DAO)
TOCTitle: CancelUpdate method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5950154d8896678889af01254104a2ac0dfef4cc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712436"
---
# <a name="recordsetcancelupdate-method-dao"></a>Метод Recordset.CancelUpdate (DAO)

**Применимо к**: Access 2013, Office 2013

Отменяет все ожидающие обновления для объекта **[набора записей](recordset-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . CancelUpdate (***UpdateType***)

*выражение* Переменная, которая представляет собой объект **набора записей** .

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Установите одно из значений <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</p><p><strong>Примечание</strong>: значения <EM>dbUpdateRegular</EM> и <EM>dbUpdateBatch</EM> действительны только в том случае, если обновление пакета включен.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Чтобы отменить все ожидающие обновления, полученный после **[изменения](recordset-edit-method-dao.md)** или **[AddNew](recordset-addnew-method-dao.md)** операции можно использовать метод **CancelUpdate** . Например если пользователь вызывает метод **AddNew** или **Изменить** и еще не вызван метод **Update** , **CancelUpdate** показано, как отменить все изменения, внесенные после **изменения** или **AddNew** вызван.

Проверьте свойство **[EditMode](recordset-editmode-property-dao.md)** **набора записей** для определения ожидающие операции, которая может быть отменена.

> [!NOTE]
> С помощью метода **CancelUpdate** имеет тот же эффект, как перейти к другой записи без с помощью метода **[Update](recordset-update-method-dao.md)** , за исключением того, что текущей записи не изменяется и не обновляются различные свойства, такие как **[BOF](recordset-bof-property-dao.md)** и **[EOF](recordset-eof-property-dao.md)**.


## <a name="example"></a>Пример

В этом примере показано использование метода **CancelUpdate** с помощью метода **AddNew** .

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
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

