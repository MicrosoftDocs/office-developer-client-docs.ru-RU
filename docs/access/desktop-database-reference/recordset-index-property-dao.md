---
title: Свойство Recordset.Index (DAO)
TOCTitle: Index Property
ms:assetid: 54626de0-eb51-31f2-bf24-e29cbfbbaa02
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194103(v=office.15)
ms:contentKeyID: 48544895
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052906
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b5f568889d020676be420186b49c9c50c444ee54
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926138"
---
# <a name="recordsetindex-property-dao"></a>Свойство Recordset.Index (DAO)

**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее имя текущего объекта **[индекса](index-object-dao.md)** в таблице тип объекта **[набора записей](recordset-object-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Индекс

*выражение* Переменная, которая представляет собой объект **набора записей** .

## <a name="remarks"></a>Примечания

Записи в базовые таблицы не сохраняются в любом порядке. Свойство **Index** изменяет порядок записей, возвращенных из базы данных; он не влияет на порядок, в котором хранятся записи.

Указанный объект **индекса** уже должны быть определены. Если значение свойства **Index** объекта **индекса** , не существует или свойства **Index** не задано, при использовании метода **[Seek](recordset-seek-method-dao.md)** , то перехватываемые возникает ошибка.

Проверьте коллекцию **индексов** **TableDef** объекта, чтобы определить, какие объекты **индекса** доступны для объектов тип таблицы **записей** , создаваемых с помощью этого объекта **TableDef** .

Можно создать новый индекс для таблицы путем создания объекта **индекса** , установка ее свойств, добавления в коллекцию **индексов** базового объекта **TableDef** и повторно открыть объекта **набора записей** .

Возвращенный объект **набора записей** в таблице типа записи могут быть упорядочены только с помощью индексов, определенных для базового объекта **TableDef** . Чтобы отсортировать записи в некоторые другие порядке, можно открыть динамический набор –, моментальный снимок – или объекта **набора записей** прямого — только — тип с помощью инструкции SQL с предложение ORDER BY.


> [!NOTE]
> - У вас нет для создания индексов для таблиц. С большой, неиндексированные таблиц доступ к определенной записи или создание объекта **набора записей** может занять много времени. С другой стороны, создание слишком много индексов замедляет работу обновления, добавлять и удалять операции, так как все индексы обновляются автоматически.
> - Чтение из таблицы без индексов записи возвращаются в определенной последовательности.
> - Свойство **[атрибуты](field-attributes-property-dao.md)** каждого объекта **[поля](field-object-dao.md)** в объекте **индекса** определяет порядок записей и следовательно определяет методы доступа для этого индекса.
> - Уникальный индекс помогает оптимизировать поиск записей.
> - Индексы не влияют на физический порядок базовая таблица индексов влияет только как записи обращением объекта **набора записей** в таблице тип при выборе определенного индекса или при открытии **набора записей** .


## <a name="example"></a>Пример

В этом примере используется свойство **индекса** Установка другой записи заказов для табличного типа **набора записей**.

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

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
