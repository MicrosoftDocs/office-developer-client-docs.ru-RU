---
title: Field.Required Property (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 77214fcad0f5b2cafe794282782df4446d37fcf6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887161"
---
# <a name="fieldrequired-property-dao"></a>Field.Required Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает, требуется ли объект **[поля](field-object-dao.md)** ненулевое значение.

## <a name="syntax"></a>Синтаксис

*выражение* . Обязательно

*выражение* Переменная, которая представляет собой объект- **поля** .

## <a name="remarks"></a>Замечания

Для **поля** еще не добавляется в конец коллекции **полей** это свойство соответствует чтения и записи.

Доступность свойства **необходимые** зависит от объекта, который содержит коллекцию [полей](fields-collection-dao.md) , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если принадлежит коллекции полей</p></th>
<th><p>Затем необходимо — это</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>индекса</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>набора записей</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p><strong>Отношения</strong> объектов</p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>TableDef</strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>


Свойства **необходимые** вместе со свойством **[пустые строки](field-allowzerolength-property-dao.md)**, **[Проверка набора](field-validateonset-property-dao.md)** или **[значение](field-validationrule-property-dao.md)** можно использовать для определения действительности значение свойства **[значение](field-value-property-dao.md)** для этого объекта **поля** . Если **требуется** свойство имеет значение **False**, поле может содержать значения **null** , а также значения, которые соответствуют условиям, указанным в параметрах свойство **пустые строки** и **значение** .


> [!NOTE]
> <P>При установке этого свойства для объекта <STRONG>индекса</STRONG> или объекта <STRONG>поля</STRONG> задайте его для объекта <STRONG>поля</STRONG> . Перед, объект <STRONG>индекса</STRONG> проверять правильность настройки свойства для объекта <STRONG>поля</STRONG> .</P>



## <a name="example"></a>Пример

В этом примере используется свойство **требуется** отчет о котором поля в три различных таблицы должен содержать данные в порядке для новой записи для добавления. Процедура RequiredOutput является обязательным для выполнения этой процедуры.

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

