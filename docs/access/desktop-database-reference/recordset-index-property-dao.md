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
localization_priority: Priority
ms.openlocfilehash: f475635424cfb9ed8ddab4025d6a944bdedd39fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300527"
---
# <a name="recordsetindex-property-dao"></a>Свойство Recordset.Index (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает имя текущего объекта **[Index](index-object-dao.md)** в объекта **[Recordset](recordset-object-dao.md)** табличного типа (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*expression* .Index

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Комментарии

Записи в базовых таблицах не хранятся в определенном порядке. Настройка свойства **Index** изменяет порядок записей, возвращаемых из базы данных; оно не влияет на порядок, в котором хранятся записи.

Указанный объект **Index** уже должен быть определен. Если вы задаете свойство **Index** для объекта **Index**, который не существует, или если свойство **Index** не задано при использовании метода **[Seek](recordset-seek-method-dao.md)**, возникает перехватываемая ошибка.

Ознакомьтесь с коллекцией **Indexes** объекта **TableDef**, чтобы определить, что объекты **Index** доступны для объектов **Recordset** табличного типа, созданных на основе объекта **TableDef**.

Вы можете создать новый индекс для таблицы, создав новый объект **Index**, задав его свойства, добавив его в коллекцию **Indexes** базового объекта **TableDef** и повторно открыв объект **Recordset**.

Записи, возвращаемые из объекта **Recordset** табличного типа, можно упорядочить только по индексам, заданным для базового объекта **TableDef**. Чтобы отсортировать записи в другом порядке, можно открыть объект **Recordset** типа dynaset, мгновенный снимок или однонаправленный с помощью оператора SQL с предложением ORDER BY.


> [!NOTE]
> - Вам не нужно создавать индексы для таблиц. Для больших, неиндексированных таблиц доступ к определенной записи или создание объекта **Recordset** может занять много времени. С другой стороны, создание слишком большого количества индексов замедляет обновление, добавление и удаление, так как все индексы автоматически обновляются.
> - Записи, считываемые из таблиц без индексов, возвращаются без определенной последовательности.
> - Свойство **[Attributes](field-attributes-property-dao.md)** каждого объекта **[Field](field-object-dao.md)** в объекте **Index** определяет порядок записей и соответственно определяет техники доступа для использования этого индекса.
> - Уникальный индекс помогает оптимизировать поиск записей.
> - Индексы не влияют на физический порядок базовой таблицы, индексы влияет только на то, как обеспечивается доступ к записям со стороны объекта **Recordset** табличного типа, когда определенный индекс выбран или открыт объект **Recordset**.


## <a name="example"></a>Пример

В этом примере используется свойство **Index** для установки другого порядка записей для объекта **Recordset** табличного типа.

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
