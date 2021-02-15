---
title: Свойство Field2.DefaultValue (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 709c9580-520e-46ce-7d70-e409872184bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195744(v=office.15)
ms:contentKeyID: 48545563
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053121
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 845a2e0c7ffa5d54d73c4fcec1a6c785468d734e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292834"
---
# <a name="field2defaultvalue-property-dao"></a>Свойство Field2.DefaultValue (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение по умолчанию для **объекта Field2.** Для объекта **Field2,** еще не присоединенного к коллекции **[Fields,](fields-collection-dao.md)** это свойство доступно только для чтения и записи (только для рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* DefaultValue

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Заметки

Значение параметра или возвращаемого значения — это **строка** типа данных, которая может содержать не более 255 символов. Это может быть текст или выражение. Если параметр свойства является выражением, он не может содержать пользовательские функции, механизм баз данных Microsoft Access SQL агрегатные функции или ссылки на запросы, формы или другие объекты **Field2.**

> [!NOTE]
> Вы также можете установить для свойства **DefaultValue** объекта **Field2** в **объекте TableDef** специальное значение под названием "GenUniqueID( )". Это приводит к присвоению этому полю случайного числа при каждом добавлении или добавлении новой записи, тем самым предоставляя каждой записи уникальный идентификатор. Свойство Type поля **должно** иметь **длину.**

Доступность свойства **DefaultValue** зависит от объекта, который содержит коллекцию **Fields,** как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит к</p></th>
<th><p>Затем значение DefaultValue</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект Index</p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p>Объект QueryDef</p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p>Объект Recordset</p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p>Объект Relation</p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p>Объект TableDef</p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>


При создании новой записи параметр **свойства DefaultValue** автоматически в качестве значения поля в качестве значения. Значение поля можно изменить, установив его свойство **Value.**

Свойство **DefaultValue** не применяется к полям **AutoNumber** и **Long Binary.**

## <a name="example"></a>Пример

В этом примере свойство **DefaultValue** используется для оповещения пользователя о нормальном значении поля при запросе ввода. Кроме того, здесь показано, как новые записи будут заполняться с помощью **DefaultValue** при отсутствии других входных данных. Для запуска этой процедуры требуется функция DefaultPrompt.

```vb
    Sub DefaultValueX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim strOldDefault As String 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strCode As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Store original DefaultValue information and set the 
     ' property to a new value. 
     strOldDefault = _ 
     tdfEmployees.Fields!PostalCode.DefaultValue 
     tdfEmployees.Fields!PostalCode.DefaultValue = "98052" 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Add a new record to the Recordset. 
     .AddNew 
     !FirstName = "Bruce" 
     !LastName = "Oberg" 
     
     ' Get user input. If user enters something, the field 
     ' will be filled with that data; otherwise, it will be 
     ' filled with the DefaultValue information. 
     strMessage = "Enter postal code for " & vbCr & _ 
     !FirstName & " " & !LastName & ":" 
     strCode = DefaultPrompt(strMessage, !PostalCode) 
     If strCode <> "" Then !PostalCode = strCode 
     .Update 
     
     ' Go to new record and print information. 
     .Bookmark = .LastModified 
     Debug.Print " FirstName = " & !FirstName 
     Debug.Print " LastName = " & !LastName 
     Debug.Print " PostalCode = " & !PostalCode 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     ' Restore original DefaultValue property because this is a 
     ' demonstration. 
     tdfEmployees.Fields!PostalCode.DefaultValue = _ 
     strOldDefault 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function DefaultPrompt(strPrompt As String, _ 
     fldTemp As Field2) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
