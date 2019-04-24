---
title: Свойство field2. Required (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6b1950c8a864fbf23bee26be89e07e49357840b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292722"
---
# <a name="field2required-property-dao"></a>Свойство field2. Required (DAO)


**Область применения**: Access 2013, Office 2013


Задает или возвращает значение, которое указывает, требуется ли для объекта **field2** значение, отличное от NULL.

## <a name="syntax"></a>Синтаксис

*Expression* . Обязательно

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Замечания

Для **field2** , еще не добавленных в коллекцию **Fields** , это свойство доступно для чтения и записи.

Доступность обязательного свойства **** зависит от объекта, содержащего коллекцию Fields, **[](fields-collection-dao.md)** как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит к элементу</p></th>
<th><p>Затем необходимо</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>Index</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>Recordset</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>Relation</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>TableDef</strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>


Свойство **Required** , Валидатеонсет или ValidationRule можно использовать вместе со свойством **AllowZeroLength**, **** или **ValidationRule** , чтобы определить допустимость параметра свойства **value** для этого объекта **field2** . Если для свойства **Required** задано значение **false**, поле может содержать значения **null** , а также значения, соответствующие условиям, заданным параметрами **пустые** и **ValidationRule** .


> [!NOTE]
> Если вы можете задать это свойство для объекта **индекса** или объекта **field2** , задайте для объекта **field2** . Допустимое значение параметра свойства для объекта **field2** проверяется до объекта **индекса** .



## <a name="example"></a>Пример

В этом примере используется свойство **Required** , чтобы сообщить, какие поля в трех различных таблицах должны содержать данные, чтобы добавить новую запись. Для выполнения этой процедуры требуется процедура Рекуиредаутпут.

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

