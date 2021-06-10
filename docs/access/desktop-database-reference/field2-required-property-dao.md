---
title: Свойство Field2.Required (DAO)
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
# <a name="field2required-property-dao"></a>Свойство Field2.Required (DAO)


**Область применения**: Access 2013, Office 2013


Задает или возвращает значение, которое указывает, требуется ли **объекту Field2** значение non-Null.

## <a name="syntax"></a>Синтаксис

*выражения* . Обязательно

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Примечания

Для **поля 2,** еще не примыкаемого к коллекции **Fields,** это свойство является чтением и написанием.

Доступность **требуемого** свойства зависит от объекта, который содержит коллекцию **[Полей,](fields-collection-dao.md)** как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит</p></th>
<th><p>Затем требуется</p></th>
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


Необходимое свойство  можно использовать вместе с свойством **AllowZeroLength,** **ValidateOnSet** или **ValidationRule** для определения действительности параметра свойства **Value** для этого объекта **Field2.** Если  необходимое свойство задано **false,** поле может содержать значения **null,** а также значения, которые соответствуют условиям, указанным в параметрах **свойств AllowZeroLength** и **ValidationRule.**


> [!NOTE]
> Если вы можете установить это свойство для объекта **Index** или **объекта Field2,** установите его для **объекта Field2.** Достоверность параметра свойства объекта **Field2** проверяется до проверки объекта **Index.**



## <a name="example"></a>Пример

В этом примере используется свойство **Required** для отчета о том, какие поля в трех разных таблицах должны содержать данные, чтобы добавить новую запись. Для запуска этой процедуры требуется процедура RequiredOutput.

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

