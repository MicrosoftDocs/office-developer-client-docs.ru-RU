---
title: Метод Fields.Append (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: ec3cacbe1f1c7ac5d6bda16bdd47891dc58ebfe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292589"
---
# <a name="fieldsappend-method-dao"></a>Метод Fields.Append (DAO)

**Область применения**: Access 2013, Office 2013

Добавляет новый объект **[Field](field-object-dao.md)** в коллекцию **[Fields](fields-collection-dao.md)**.

## <a name="syntax"></a>Синтаксис

*выражение* .Append(***Object***)

*выражение*: переменная, представляющая объект **Fields**.

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
<td><p><em>Object</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Object</strong></p></td>
<td><p>Объектная переменная, представляющая поле, которое добавляется в коллекцию.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Метод **Append** можно использовать для добавления новой таблицы в базу данных, добавления поля в таблицу и добавления поля в индекс.

Добавляемый объект становится постоянным объектом, хранящимся на диске, пока вы не удалите его с помощью метода **Delete**.

Добавление нового объекта происходит незамедлительно, но следует применить метод **Refresh** для любых других коллекций, которые могут быть затронуты изменениями в структуре базы данных.

Если добавляемый объект неполный (например, если не добавлены объекты **Field** в коллекцию **Fields** объекта **Index** перед его добавлением в коллекцию **Indexes**) или заданы неверные свойства в одном или нескольких подчиненных объектах, применение метода **Append** вызывает ошибку. Например, если не указан тип поля и выполняется попытка добавить объект **Field** в коллекцию **Fields** объекта **TableDef**, применение метода **Append** вызывает ошибку во время выполнения.

## <a name="example"></a>Пример

В этом примере используется метод **Append** или метод **Delete** для изменения коллекции **Fields** объекта **TableDef**. Процедура AppendDeleteField является обязательной для запуска этой процедуры.

```vb
    Sub AppendX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Add three new fields. 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "E-mail", dbText, 50 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Http", dbText, 80 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Quota", dbInteger, 5 
     
     Debug.Print "Fields after Append" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show the new fields. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     ' Delete the newly added fields. 
     AppendDeleteField tdfEmployees, "DELETE", "E-mail" 
     AppendDeleteField tdfEmployees, "DELETE", "Http" 
     AppendDeleteField tdfEmployees, "DELETE", "Quota" 
     
     Debug.Print "Fields after Delete" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show that the new 
     ' fields have been deleted. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub AppendDeleteField(tdfTemp As TableDef, _ 
     strCommand As String, strName As String, _ 
     Optional varType, Optional varSize) 
     
     With tdfTemp 
     
     ' Check first to see if the TableDef object is 
     ' updatable. If it isn't, control is passed back to 
     ' the calling procedure. 
     If .Updatable = False Then 
     MsgBox "TableDef not Updatable! " & _ 
     "Unable to complete task." 
     Exit Sub 
     End If 
     
     ' Depending on the passed data, append or delete a 
     ' field to the Fields collection of the specified 
     ' TableDef object. 
     If strCommand = "APPEND" Then 
     .Fields.Append .CreateField(strName, _ 
     varType, varSize) 
     Else 
     If strCommand = "DELETE" Then .Fields.Delete _ 
     strName 
     End If 
     
     End With 
     
    End Sub
```
