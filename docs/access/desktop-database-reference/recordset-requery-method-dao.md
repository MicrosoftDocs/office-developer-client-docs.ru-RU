---
title: Метод Recordset.Requery (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8405cf2f8d6eea7ce0e55bb543510db6242be84a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919089"
---
# <a name="recordsetrequery-method-dao"></a>Метод Recordset.Requery (DAO)


**Применимо к**: Access 2013, Office 2013

Обновляет данные в объект **[набора записей](recordset-object-dao.md)** , повторное выполнение запросов, на котором основан объект.

## <a name="syntax"></a>Синтаксис

*выражение* . Обновление (***NewQueryDef***)

*выражение* Переменная, которая представляет собой объект **набора записей** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NewQueryDef</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Представляет значение свойства <strong>Name</strong> объекта <strong><a href="querydef-object-dao.md">QueryDef</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Используйте этот метод, чтобы убедиться в том, что **набор записей** содержит последние данные. Этот метод повторно заполняет текущего **набора записей** с помощью любого из текущего запроса или (в рабочей области для Microsoft Access) новых структур указано в аргументе newquerydef.

Если не указан аргумент newquerydef, **записей** повторно заполняется на основе одного определения запроса и параметры, используемые для заполнения изначально **набора записей**. Любые изменения в базовые данные будут отражены во время повторного заполнения. Если **QueryDef** не используется для создания **записей**, **записей** повторно создать с нуля.

При указании исходного **QueryDef** в аргументе newquerydef, затем **записей** обновляется с использованием параметров, указанного идентификатором **QueryDef**. Любые изменения в базовые данные будут отражены во время повторного заполнения. Чтобы отразить любые изменения значения параметров запроса в **набор записей**, необходимо указать аргумент newquerydef.

Если указать другой **QueryDef** чем что использовалась для создания **записей** **набора записей** повторно создать с нуля.

При использовании **повторный запрос**первой записи в **набор записей** становится текущей.

Нельзя использовать метод **повторный запрос** на или моментальный снимок добавляющий объектов **наборов записей** , свойство **[Restartable](recordset-restartable-property-dao.md)** имеет значение **False**. Тем не менее если вы задаете newquerydef необязательный аргумент, свойство **Restartable** игнорируется.

Если **как **[BOF](recordset-bof-property-dao.md)** , так и параметры свойства **[EOF](recordset-eof-property-dao.md)** объекта **набора записей** выполняются после использования метода **повторный запрос** ,** запрос не возвращает никаких записей и **записей** не содержит данных.

## <a name="example"></a>Пример

В этом примере показано использование метода **повторный запрос** для обновления запроса после изменения базовых данных.

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset 
     Dim rstChange As Recordset 
     
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

В этом примере показано использование метода **повторный запрос** для обновления запроса после изменения параметров запроса.

```vb 
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset 
 
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

