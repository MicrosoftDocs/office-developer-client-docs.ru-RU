---
title: Метод Recordset.Seek (DAO)
TOCTitle: Seek Method
ms:assetid: ef83d909-c962-b016-7d33-36eacdc25c2c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836416(v=office.15)
ms:contentKeyID: 48548585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053061
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b86713870efb2ed5974f462197cadc95df43fcb3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920776"
---
# <a name="recordsetseek-method-dao"></a>Метод Recordset.Seek (DAO)

**Применимо к**: Access 2013, Office 2013

Указывает расположение записи в объекте **набора записей** индексированных тип таблицы, которая должна удовлетворять определенным условиям для текущего индекса и делает, запишите текущей записи (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Поиск (***сравнения***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)

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
<td><p>Comparison</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Один из следующих строковых выражений: &lt;, &lt;=, =, &gt;=, или &gt;.</p></td>
</tr>
<tr class="even">
<td><p>Key1 Key2... Key13</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Один или несколько значения, соответствующие поля в текущий индекс объекта <strong>набора записей</strong> в соответствии с его значение свойства <strong>Index</strong> . Можно использовать до 13 ключевые аргументов.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Прежде чем использовать **Seek**необходимо задать текущего индекса с помощью свойства **индекса** . Если индекс определяет неуникальные ключевое поле, **Seek** находит первой записи, соответствующие этим условиям.

Метод **Seek** просматривает указанный ключевых полей и указывает расположение первой записи, которая должна удовлетворять условиям, указанным для сравнения и key1. После нахождения его делает этой записи текущего и устанавливает для свойства **NoMatch** значение **False**. При сбое метода **Seek** для поиска соответствия, свойство **NoMatch** имеет значение **True**, а текущей записи не определен.

Если сравнения равенства (=), больше или равно (\>=), больше или равно (\>), **Seek** начинается с начала индекса и поиск.

Если сравнение меньше, чем (\<) или меньше или равно (\<=), запускается после окончания индекс **поиска** и выполняет поиск. Тем не менее если индекс записи в конце индекса, **Seek** начинается с произвольной запись между дубликаты и затем выполняет поиск.

Необходимо указать значения для всех полей, определенных в индексе. При использовании **поиска** с несколькими столбцами индекса и не указать значение для сравнения для каждого поля в индексе, оператор равенства (=) нельзя использовать для сравнения. Вот так как некоторые критерии поля (key2, key3 и т. д.) будет по умолчанию назначается значение Null, при котором скорее всего, не будет соответствовать. Таким образом равно будет работать правильно только в том случае, если у вас есть записи, которая представляет все **значение null,** за исключением ключ, который вы ищете. Рекомендуется использовать больше или равно (\>=) оператор вместо этого.

Аргумент key1 должен быть типу данных поля в соответствующее поле в текущем индекса. Например если текущий индекс ссылается числовое поле (например, идентификатор сотрудника), key1 должен быть числовым. Аналогично Если текущий индекс ссылается на поле текст (Фамилия), key1 должна быть строка.

Существует не должен быть текущей записи при использовании **поиска**.

Коллекции **[индексов](indexes-collection-dao.md)** можно использовать для перечисления существующие индексы.

Чтобы найти записи в или моментальный снимок добавляющий **записей** , которая должна удовлетворять определенное условие, которое не принадлежат существующих индексов, используйте методы **[Найти](recordset-findfirst-method-dao.md)** . Чтобы включить все записи, не только те, которые удовлетворяют определенному условию использовать методы **[перемещения](recordset-movefirst-method-dao.md)** для перемещения по записям.

Нельзя использовать метод **Seek** в связанной таблицы, так как не удается открыть связанные таблицы как в таблице объекты **набора записей** . Тем не менее при использовании метода **[OpenDatabase](dbengine-opendatabase-method-dao.md)** непосредственно открыть базу данных устанавливаемый драйвер ISAM (не являющиеся ODBC) можно использовать **Seek** для таблиц в базе данных.

## <a name="example"></a>Пример

В этом примере демонстрируется использование метода **Seek** , позволяя пользователю выполнять поиск по идентификатору продукта.

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
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
       Dim rstProducts As Recordset 
       Dim rstCustomers As Recordset 
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

<br/>

Следующем примере показано, как использовать метод поиска для поиска записей в связанной таблице.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
