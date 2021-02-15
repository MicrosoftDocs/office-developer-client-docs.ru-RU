---
title: Свойство Field.Required (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 52900d4a60002695866b9960fb6b80cefeb2b2ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292981"
---
# <a name="fieldrequired-property-dao"></a>Свойство Field.Required (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает, требуется ли для объекта **[Field](field-object-dao.md)** значение, не относящеся к NULL.

## <a name="syntax"></a>Синтаксис

*выражение .* Обязательно

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Для **поля,** еще не примежаемого к коллекции **Fields,** это свойство доступно для чтения и записи.

Доступность обязательного **свойства** зависит от объекта, который содержит коллекцию [Fields,](fields-collection-dao.md) как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит к</p></th>
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


Вы можете  использовать обязательное свойство вместе со свойством **[AllowZeroLength,](field-allowzerolength-property-dao.md)** **[ValidateOnSet](field-validateonset-property-dao.md)** или **[ValidationRule,](field-validationrule-property-dao.md)** чтобы определить допустимый срок действия параметра свойства **[Value](field-value-property-dao.md)** для этого объекта **Field.** Если свойство **Required** имеет значение **False,** поле может содержать значения **null,** а также значения, которые соответствуют условиям, указанным в параметрах свойств **AllowZeroLength** и **ValidationRule.**


> [!NOTE]
> Если вы можете установить это свойство для объекта **Index** или **Объекта Field,** установите его для **объекта Field.** Срок действия параметра свойства для объекта **Field** проверяется до того, как он находится в **объекте Index.**



## <a name="example"></a>Пример

В этом примере свойство **Required** используется для сообщения о том, какие поля в трех разных таблицах должны содержать данные, чтобы добавить новую запись. Для запуска этой процедуры требуется процедура RequiredOutput.

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
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

