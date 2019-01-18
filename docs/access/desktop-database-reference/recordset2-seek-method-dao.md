---
title: Метод Recordset2.Seek (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9510faab9035f2b2cbcccae0a8ddefa484a95cb1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700649"
---
# <a name="recordset2seek-method-dao"></a>Метод Recordset2.Seek (DAO)

**Применимо к**: Access 2013, Office 2013

Указывает расположение записи в объекте **набора записей** индексированных тип таблицы, которая должна удовлетворять определенным условиям для текущего индекса и делает, запишите текущей записи (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Поиск (***сравнения***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Comparison</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Один из следующих строковых выражений: &lt;, &lt;=, =, &gt;=, или &gt;.</p></td>
</tr>
<tr class="even">
<td><p><em>Key1 Key2... Key13</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Один или несколько значения, соответствующие поля в текущий индекс объекта <strong>набора записей</strong> в соответствии с его значение свойства <strong>Index</strong> . Можно использовать до 13 ключевые аргументов.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Прежде чем использовать **Seek**необходимо задать текущего индекса с помощью свойства **индекса** . Если индекс определяет неуникальные ключевое поле, **Seek** находит первой записи, соответствующие этим условиям.

Метод **Seek** просматривает указанный ключевых полей и указывает расположение первой записи, которая должна удовлетворять условиям, указанным для сравнения и key1. После нахождения его делает этой записи текущего и устанавливает для свойства **NoMatch** значение **False**. При сбое метода **Seek** для поиска соответствия, свойство **NoMatch** имеет значение **True**, а текущей записи не определен.

Если сравнения равенства (=), больше или равно (\>=), больше или равно (\>), **Seek** начинается с начала индекса и поиск.

Если сравнение меньше, чем (\<) или меньше или равно (\<=), запускается после окончания индекс **поиска** и выполняет поиск. Тем не менее если индекс записи в конце индекса, **Seek** начинается с произвольной запись между дубликаты и затем выполняет поиск.

Необходимо указать значения для всех полей, определенных в индексе. При использовании **поиска** с несколькими столбцами индекса и не указать значение для сравнения для каждого поля в индексе, оператор равенства (=) нельзя использовать для сравнения. Вот так как некоторые критерии поля (key2, key3 и т. д.) будет по умолчанию назначается значение Null, при котором скорее всего, не будет соответствовать. Таким образом равно будет работать правильно только в том случае, если у вас есть записи, которая представляет все **значение null,** за исключением ключ, который вы ищете. Рекомендуется использовать больше или равно (\>=) оператор вместо этого.

Аргумент key1 должен быть типу данных поля в соответствующее поле в текущем индекса. Например если текущий индекс ссылается числовое поле (например, идентификатор сотрудника), key1 должен быть числовым. Аналогично Если текущий индекс ссылается на поле текст (Фамилия), key1 должна быть строка.

Существует не должен быть текущей записи при использовании **поиска**.

Коллекции **[индексов](indexes-collection-dao.md)** можно использовать для перечисления существующие индексы.

Чтобы найти записи в или моментальный снимок добавляющий **записей** , которая должна удовлетворять определенное условие, которое не принадлежат существующих индексов, используйте методы **[Найти](recordset2-findfirst-method-dao.md)** . Чтобы включить все записи, не только те, которые удовлетворяют определенному условию использовать методы **[перемещения](recordset-movefirst-method-dao.md)** для перемещения по записям.

Нельзя использовать метод **Seek** в связанной таблицы, так как не удается открыть связанные таблицы как в таблице объекты **набора записей** . Тем не менее при использовании метода **[OpenDatabase](dbengine-opendatabase-method-dao.md)** непосредственно открыть базу данных устанавливаемый драйвер ISAM (не являющиеся ODBC) можно использовать **Seek** для таблиц в базе данных.

## <a name="example"></a>Пример

В этом примере демонстрируется использование метода **Seek** , позволяя пользователю выполнять поиск по идентификатору продукта.

```vb
    Sub SeekX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim intFirst As Integer 
     Dim intLast As Integer 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' You must open a table-type Recordset to use an index, 
     ' and hence the Seek method. 
     Set rstProducts = _ 
     dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
     With rstProducts 
     ' Set the index. 
     .Index = "PrimaryKey" 
     
     ' Get the lowest and highest product IDs. 
     .MoveLast 
     intLast = !ProductID 
     .MoveFirst 
     intFirst = !ProductID 
     
     Do While True 
     ' Display current record information and ask user 
     ' for ID number. 
     strMessage = "Product ID: " & !ProductID & vbCr & _ 
     "Name: " & !ProductName & vbCr & vbCr & _ 
     "Enter a product ID between " & intFirst & _ 
     " and " & intLast & "." 
     strSeek = InputBox(strMessage) 
     
     If strSeek = "" Then Exit Do 
     
     ' Store current bookmark in case the Seek fails. 
     varBookmark = .Bookmark 
     
     .Seek "=", Val(strSeek) 
     
     ' Return to the current record if the Seek fails. 
     If .NoMatch Then 
     MsgBox "ID not found!" 
     .Bookmark = varBookmark 
     End If 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

В этом примере используется свойство **NoMatch** для определения ли **Seek** и **FindFirst** было выполнено успешно и если это не так, чтобы предоставить соответствующий отзыв. Процедуры SeekMatch и FindMatch необходимы для выполнения этой процедуры.

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```
