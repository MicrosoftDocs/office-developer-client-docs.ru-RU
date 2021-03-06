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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300681"
---
# <a name="recordsetcancelupdate-method-dao"></a>Метод Recordset.CancelUpdate (DAO)

**Область применения**: Access 2013, Office 2013

Отменяет любые незавершенные обновления для объекта **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*выражения* . CancelUpdate ***(UpdateType)***

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
<td><p>Установите одно из <strong><a href="updatetypeenum-enumeration-dao.md">значений UpdateTypeEnum.</a></strong></p><p><strong>ПРИМЕЧАНИЕ.</strong>Значения <EM>dbUpdateRegular</EM> и <EM>dbUpdateBatch</EM> действительны только при включенной пакетной обновлении.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

С помощью метода **CancelUpdate** можно отменить все ожидающие обновления в результате операции **[Edit](recordset-edit-method-dao.md)** или **[AddNew.](recordset-addnew-method-dao.md)** Например, если пользователь вызывает метод **Edit** или **AddNew** и еще  не вызывает метод **Update, CancelUpdate** отменяет любые изменения, внесенные после вызова **Edit** или **AddNew.**

Проверьте свойство **[EditMode](recordset-editmode-property-dao.md)** в **Наборе записей,** чтобы определить, существует ли ожидаемая операция, которую можно отменить.

> [!NOTE]
> Использование метода **CancelUpdate** имеет тот же эффект, что **[](recordset-update-method-dao.md)** и переход на другую запись без использования метода Update, за исключением того, что текущая запись не меняется, а различные свойства, такие как **[BOF](recordset-bof-property-dao.md)** и **[EOF,](recordset-eof-property-dao.md)** не обновляются.


## <a name="example"></a>Пример

В этом примере показано, как метод **CancelUpdate** используется с **методом AddNew.**

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

В этом примере показано, как метод **CancelUpdate** используется с методом **Редактирование.**

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

