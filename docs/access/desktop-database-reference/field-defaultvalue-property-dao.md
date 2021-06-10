---
title: Свойство Field.DefaultValue (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 8a1c558b-c8f6-757d-c595-4e50b9b6ae3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197092(v=office.15)
ms:contentKeyID: 48546185
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fb4d3a4427db2b407b6a20507339fe83665c97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293121"
---
# <a name="fielddefaultvalue-property-dao"></a>Свойство Field.DefaultValue (DAO)


**Область применения**: Access 2013, Office 2013


Задает или возвращает значение по умолчанию объекта **[Field.](field-object-dao.md)** Для объекта **Field,** еще не присоединенного к коллекции **[Fields,](fields-collection-dao.md)** это свойство является чтением или записью (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . DefaultValue

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Значение параметра или возврата — это **тип данных String,** который может содержать не более 255 символов. Это может быть текст или выражение. Если параметр свойства является выражением, он не может содержать определенные пользователем функции, двигатель базы данных Microsoft Access SQL совокупные функции или ссылки на запросы, формы или другие объекты **Field.**


> [!NOTE]
> Можно также установить свойство **DefaultValue** объекта **Field** на [объекте TableDef](tabledef-object-dao.md) к специальному значению под названием "GenUniqueID()". Это приводит к присвоению случайного номера этому полю всякий раз, когда новая запись добавляется или создается, тем самым предоставляя каждой записи уникальный идентификатор. Свойство Type поля [должно](field-type-property-dao.md) быть **Long**.


Доступность свойства **DefaultValue** зависит от объекта, который содержит коллекцию **Полей,** как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит</p></th>
<th><p>Затем DefaultValue</p></th>
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


При создании новой записи параметр **свойства DefaultValue** автоматически вписается в качестве значения для поля. Значение поля можно изменить, установив его свойство **[Value.](field-value-property-dao.md)**

Свойство **DefaultValue** не применяется к **полям AutoNumber** и **Long Binary.**

## <a name="example"></a>Пример

В этом примере свойство **DefaultValue** используется для оповещения пользователя о нормальном значении поля при запросе ввода. Кроме того, в нем показано, как будут заполняться новые записи с **помощью DefaultValue** при отсутствии других входных данных. Для запуска этой процедуры требуется функция DefaultPrompt.

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
     fldTemp As Field) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
