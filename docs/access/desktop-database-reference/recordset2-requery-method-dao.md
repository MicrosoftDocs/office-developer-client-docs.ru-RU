---
title: Метод Recordset2. Requery (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44f573d179c26677fc801dac82e0deecc3874fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307212"
---
# <a name="recordset2requery-method-dao"></a>Метод Recordset2. Requery (DAO)

**Область применения**: Access 2013, Office 2013

Обновляет данные в объекте **[Recordset](recordset-object-dao.md)** с помощью повторного выполнения запроса, на котором основан объект.

## <a name="syntax"></a>Синтаксис

*выражение* .Requery(***NewQueryDef***)

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

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
<td><p><em>NewQueryDef</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Представляет значение свойства <strong>Name</strong> объекта <strong><a href="querydef-object-dao.md">QueryDef</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Используйте этот метод, чтобы обеспечить наличие самых последних данных в объекте **Recordset**. Этот метод повторно заполняет текущий объект **Recordset** с помощью текущих параметров запроса или (в рабочей области Microsoft Access) новыми параметрами, предоставляемыми аргументом newquerydef.

Если аргумент newquerydef не указан, объект **Recordset** повторно заполняется на основе того же определения запроса и параметров, использованных изначально для заполнения объекта **Recordset**. Все изменения базовых данных будут отражены во время этого повторного заполнения. Если вы не используете объект **QueryDef** для создания объекта **Recordset**, **Recordset** повторно создается с нуля.

Если в аргументе newquerydef указан исходный объект **QueryDef**, объект **Recordset** повторно запрашивается с помощью параметров, указанных объектом **QueryDef**. Все изменения базовых данных будут отражены во время этого повторного заполнения. Чтобы отразить любые изменения значений параметров запроса в объекте **Recordset**, необходимо указать аргумент newquerydef.

Если указать другой объект **QueryDef** вместо использованного изначально для создания объекта **Recordset**, **Recordset** повторно создается с нуля.

При использовании метода **Requery** первая запись в объекте **Recordset** становится текущей записью.

Вы не можете использовать метод **Requery** для объектов **Recordset** типа "Динамический набор" или "Статический набор", свойству **[Restartable](recordset2-restartable-property-dao.md)** которых присвоено значение **False**. Но если указан необязательный аргумент newquerydef, свойство **Restartable** игнорируется.

Если свойствам **[BOF](recordset2-bof-property-dao.md)** и **[EOF](recordset2-eof-property-dao.md)** объекта **Recordset** присвоено значение **True** после использования метода **Requery**, запрос не возвращает какие-либо записи и объект **Recordset** не содержит данных.

## <a name="example"></a>Пример

В этом примере показано, как можно использовать метод **Requery** для обновления запроса после изменения базовых данных.

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

В этом примере показано, как можно использовать метод **Requery** для обновления запроса после изменения параметров запроса.

```vb
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset2 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

