---
title: Field.DefaultValue Property (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 8a1c558b-c8f6-757d-c595-4e50b9b6ae3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197092(v=office.15)
ms:contentKeyID: 48546185
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4a2710c714f22ad7ec1a27dc3e4750f56d6fac5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891095"
---
# <a name="fielddefaultvalue-property-dao"></a>Field.DefaultValue Property (DAO)


**Применимо к**: Access 2013, Office 2013


Задает или возвращает значение по умолчанию объекта **[поля](field-object-dao.md)** . Для объекта **поля** , еще не добавляется в конец коллекции **[полей](fields-collection-dao.md)** это свойство является чтение/запись (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Значение по умолчанию

*выражение* Переменная, которая представляет собой объект- **поля** .

## <a name="remarks"></a>Замечания

Параметр или возвращаемое значение имеет тип данных **String** , которое может содержать не более 255 знаков. Она может быть текст или выражение. Если значение свойства — это выражение, не может содержать пользовательские функции, статистические функции ядра базы данных SQL Microsoft Access или ссылки на запросы, форм или других объектов **поля** .


> [!NOTE]
> Также можно настроить свойство **DefaultValue** объекта **поля** на объект [TableDef](tabledef-object-dao.md) особое значение называется «(GenUniqueID)». В результате случайное число для назначения в этом поле каждый раз, когда добавляется или создать новую запись, тем самым обеспечивая каждой записи уникального идентификатора. [Тип](field-type-property-dao.md) поля должен быть **времени**.


Доступность **функции DefaultValue** зависит от объекта, который содержит коллекцию **полей** , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если принадлежит коллекции полей</p></th>
<th><p>Значение по умолчанию — это</p></th>
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


При создании новой записи, значение свойства **DefaultValue** автоматически вводится как значение для поля. Значение поля можно изменить, задав его свойство **[Value](field-value-property-dao.md)** .

Свойство **DefaultValue** не применяется к **счетчика** и **Длинные двоичные** поля.

## <a name="example"></a>Пример

В этом примере используется свойство **DefaultValue** для оповещения пользователя Обычное значение поля во время запроса на ввода данных. Кроме того, он показывает, как новые записи будет состоять из с помощью **DefaultValue** при отсутствии другие входные данные. Функция DefaultPrompt является обязательным для выполнения этой процедуры.

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
