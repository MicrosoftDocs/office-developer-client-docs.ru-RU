---
title: Свойство field2. DefaultValue (DAO)
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
# <a name="field2defaultvalue-property-dao"></a>Свойство field2. DefaultValue (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, заданное по умолчанию для объекта **field2** . Для объекта **field2** , еще не добавленного в коллекцию **[Fields](fields-collection-dao.md)** , это свойство доступно для чтения и записи (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . Значение

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Замечания

Параметр или возвращаемое значение — это **строковый** тип данных, который может содержать не более 255 символов. Это может быть либо Text, либо Expression. Если параметр свойства является выражением, он не может содержать пользовательские функции, статистические функции SQL ядра СУБД Microsoft Access или ссылки на запросы, формы или другие объекты **field2** .

> [!NOTE]
> Кроме того, можно задать для свойства **DefaultValue** объекта **field2** в объекте **tabledef** специальное значение с именем "женуникуеид ()". Это приводит к тому, что это поле назначается случайному числу при добавлении или создании новой записи, таким образом выдавая каждой записи уникальный идентификатор. Свойство **типа** поля должно быть длинным ****.

Доступность свойства **DefaultValue** зависит от объекта, содержащего коллекцию Fields, как **** показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит к элементу</p></th>
<th><p>Значение DefaultValue</p></th>
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


При создании новой записи параметр свойства **DefaultValue** автоматически вводится в качестве значения для поля. Значение поля можно изменить, задав его свойство **value** .

Свойство **DefaultValue** не применяется к полям **счетчика** и **длинным двоичным** полям.

## <a name="example"></a>Пример

В этом примере используется свойство **DefaultValue** для оповещения пользователя о обычном значении поля при запросе ввода. Кроме того, в нем показано, как новые записи будут заполнены с использованием **DefaultValue** при отсутствии других входных данных. Для выполнения этой процедуры требуется функция Дефаултпромпт.

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
