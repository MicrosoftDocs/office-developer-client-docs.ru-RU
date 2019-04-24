---
title: Метод Recordset2. reQuery (DAO)
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
# <a name="recordset2requery-method-dao"></a>Метод Recordset2. reQuery (DAO)

**Область применения**: Access 2013, Office 2013

Обновляет данные в объекте **[Recordset](recordset-object-dao.md)** с помощью повторного выполнения запроса, на котором основан объект.

## <a name="syntax"></a>Синтаксис

*Expression* . ReQuery (***невкуеридеф***)

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
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Невкуеридеф</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Представляет значение свойства <strong>имени</strong> объекта <strong><a href="querydef-object-dao.md">QueryDef</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Используйте этот метод, чтобы убедиться, что объект **Recordset** содержит самые последние данные. Этот метод повторно заполняет текущий **набор записей** с помощью текущих параметров запроса или (в рабочей области Microsoft Access) новыми, которые предоставляются аргументом невкуеридеф.

Если не указать аргумент невкуеридеф, то **набор записей** повторно заполняется в соответствии с тем же определением запроса и параметрами, которые использовались для первоначального заполнения объекта **Recordset**. Все изменения базовых данных будут отражены во время этого повторного заполнения. Если для создания объекта **Recordset**не использовался объект **QueryDef** , то **набор записей** повторно создается с нуля.

Если вы укажете исходный объект **QueryDef** в аргументе невкуеридеф, то этот **набор записей** будет повторно запрашиваться с использованием параметров, заданных объектом **QueryDef**. Все изменения базовых данных будут отражены во время этого повторного заполнения. Чтобы отразить любые изменения значений параметров запроса в наборе **записей**, необходимо указать аргумент невкуеридеф.

Если указать другой объект **QueryDef** , отличный от первоначально использованного для создания **набора записей**, то **набор записей** повторно создается с нуля.

При использовании **запроса Requery**первая запись в наборе **записей** становится текущей записью.

Невозможно использовать метод **restart** для объектов **Recordset** типа динамического подмножества или моментального снимка, для свойства restarted которого задано значение **false**. **[](recordset2-restartable-property-dao.md)** Однако при указании необязательного аргумента невкуеридеф свойство **** restarted игнорируется.

Если параметры свойств **[BOF](recordset2-bof-property-dao.md)** и **[EOF](recordset2-eof-property-dao.md)** объекта **Recordset** имеют **значение true** после использования метода Requery, то **** запрос не возвращал какие бы то ни было записи, а объект **Recordset** не содержит данных.

## <a name="example"></a>Пример

В этом примере показано, **** как можно использовать метод Requery для обновления запроса после изменения базовых данных.

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

В этом примере показано, **** как можно использовать метод Requery для обновления запроса после изменения параметров запроса.

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

