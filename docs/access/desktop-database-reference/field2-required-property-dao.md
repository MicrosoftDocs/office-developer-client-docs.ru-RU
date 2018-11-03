---
title: Свойство Field2.Required (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf5e459773cd0fa0976704834b1b73467fc75294
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937409"
---
# <a name="field2required-property-dao"></a>Свойство Field2.Required (DAO)


**Применимо к**: Access 2013, Office 2013


Задает или возвращает значение, которое указывает, требуется ли объект **поле2** ненулевое значение.

## <a name="syntax"></a>Синтаксис

*выражение* . Обязательно

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Примечания

Для **поле2** еще не добавляется в конец коллекции **полей** это свойство соответствует чтения и записи.

Доступность свойства **необходимые** зависит от объекта, который содержит коллекцию **[полей](fields-collection-dao.md)** , как показано в следующей таблице.

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


Свойства **необходимые** вместе со свойством **пустые строки**, **Проверка набора**или **значение** можно использовать для определения действительности параметр свойства **Value** объекта **поле2** . Если **требуется** свойство имеет значение **False**, поле может содержать значения **null** , а также значения, которые соответствуют условиям, указанным в параметрах свойство **пустые строки** и **значение** .


> [!NOTE]
> При установке этого свойства для объекта **индекса** или объект **поле2** устанавливалось для объекта **поле2** . Действия значение свойства для объекта **поле2** проверяется до этого объекта **индекса** .



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

