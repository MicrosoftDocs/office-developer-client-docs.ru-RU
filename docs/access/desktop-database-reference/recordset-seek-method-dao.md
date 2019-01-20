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
localization_priority: Priority
ms.openlocfilehash: db2c90d42feacee58af9eea30a2d99439cb4ddaf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708895"
---
# <a name="recordsetseek-method-dao"></a>Метод Recordset.Seek (DAO)

**Область применения**: Access 2013, Office 2013

Определяет положение записи в индексированном объекте**Recordset** табличного типа, которое отвечает заданным условиям для текущего индекса и превращает данную запись в текущую запись (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)

*expression*: переменная, представляющая объект **Recordset**.

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
<td><p><em>Comparison</em></p></td>
<td><p>Обязательно</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Один из приведенных ниже выражений строки: &lt;, &lt;=, =, &gt;=, or &gt;.</p></td>
</tr>
<tr class="even">
<td><p><em>Key1, Key2...Key13</em></p></td>
<td><p>Обязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Один или несколько значений, соответствующих полям в текущем индексе объекта <strong>Recordset</strong>, как указано в настройках свойства <strong>Index</strong>. Вы можете использовать до 13 ключевых аргументов.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Комментарии

Необходимо задать текущий индекс со свойством **Index**, прежде чем вы сможете использовать **Seek**. Если индекс обнаруживает неуникальное поле ключа, **Seek** определяет положение первой записи, которая удовлетворяет условиям.

Метод **Seek** выполняет поиск по указанным ключевым полям и определяет положение первой записи, которая удовлетворяет условиям, заданным сравнением и значением key1. После обнаружения он запись текущей и задает значение **False** для свойства **NoMatch**. Если методу **Seek** не удалось найти совпадение, для свойства **NoMatch** задается значение **True**, а текущая запись остается без определения.

Если сравнение равно (=), больше или равно (\>=), либо больше, чем (\>), **Seek** начинает поиск с начала индекса и выполняет поиск вперед.

Если сравнение меньше, чем (\<) или меньше или равно (\<=), **Seek** начинает поиск с конца индекса и выполняет поиск в обратном порядке. Тем не менее, если есть повторяющиеся записи в индексе в конце индекса, **Seek** начинает поиск с произвольного элемента среди повторяющихся записей и затем выполняет поиск в обратном направлении.

Необходимо указать значения для всех полей, определенных в индексе. Если вы используете **Seek** с индексом с несколькими столбцами и вы не указываете значение сравнения для каждого поля в индексе,тогда в сравнение вы не сможете использовать оператор равенства (=). Дело в том, что некоторые поля условий (key2, key3 и т. д.), будут по умолчанию иметь значение Null, которое, возможно, не будет совпадать. Таким образом, оператор равенства будет работать правильно только в том случае, если у вас есть запись со значением**null**, за исключением ключа, которое вы ищете. Мы рекомендуем использовать оператор больше или равно (\>=).

Аргумент key1 должен относится к тому же типу поля данных, что и соответствующее поле в текущем индексе. Например если текущий индекс ссылается на числовое поле (например, код сотрудника), key1 должен иметь числовое значение. Аналогичным образом, если текущий индекс ссылается на текстовое поле (например, фамилия), key1 должен быть строкой.

Вам не нужно использовать текущую запись при использовании **Seek**.

Вы можете использовать коллекцию **[Indexes](indexes-collection-dao.md)** для перечисления существующих индексов.

Чтобы найти запись в объекте **Recordset** типа dynaset или мгновенный снимок, удовлетворяющую определенным условиям, которое не распространяются на существующие индексы, используйте методы **[Find](recordset-findfirst-method-dao.md)**. Чтобы включить все записи, а не только те, которые удовлетворяют заданному условию, используйте методы **[Move](recordset-movefirst-method-dao.md)**, чтобы перейти из записи.

Вы не можете использовать метод **Seek** для связанной таблицы, так как вы не сможете открыть связанные таблицы в виде объекта **Recordset** табличного типа. Тем не менее если вы используете метод **[OpenDatabase](dbengine-opendatabase-method-dao.md)**, чтобы открыть устанавливаемую базу данных ISAM (не ODBC), вы можете использовать **Seek** для таблиц в этой базе.

## <a name="example"></a>Пример

В этом примере показан метод **Seek**, позволяющий пользователю выполнить поиск продукта на основании на номере идентификатора.

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

В этом примере используется свойство **NoMatch** для определения того, принесли ли результат методы **Seek** и **FindFirst**, и если нет, обеспечение соответствующей реакции. Процедуры SeekMatch и FindMatch являются обязательными для запуска этой процедуры.

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

В приведенном ниже примере показано, как использовать метод Seek для поиска записи в связанной таблице.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
