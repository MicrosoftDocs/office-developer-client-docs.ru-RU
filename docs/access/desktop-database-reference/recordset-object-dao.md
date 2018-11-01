---
title: Recordset Object (DAO)
TOCTitle: Recordset Object
ms:assetid: 9774232c-e6da-175b-fc7f-ed2ab7908fa0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197799(v=office.15)
ms:contentKeyID: 48546469
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df3b2e8d0d5cba07a826a83098187b911f19a3a2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871971"
---
# <a name="recordset-object-dao"></a>Recordset Object (DAO)

**Применимо к**: Access 2013, Office 2013

Объект **набора записей** представляет записей в базовой таблице или записей, в результате выполнения запроса.

## <a name="remarks"></a>Замечания

Для работы с данными в базе данных на уровне записей используйте объекты **набора записей** . При использовании объектов DAO работы с данным почти полностью с помощью объектов **набора записей** . Все объекты **наборов записей** , созданные с помощью записей (строк) и полей (столбцов). Существует пять типов объектов **набора записей** .

- Тип таблицы записей — представление в коде базовой таблицы, которые можно использовать для добавления, изменения или удаления записей из одной таблицы базы данных (только для рабочих областей Microsoft Access).

- Копирование или изменение — результат запроса, который может иметь обновляемых записей. Объект **набора записей** добавляющий представляют собой динамический набор записей, которые можно использовать для добавления, изменения или удаления записей из базовой таблицы базы данных или таблицы. Объект типа динамического **набора записей** может содержать поля из одного или нескольких таблиц в базе данных. Этот тип соответствует курсор набора ключей ODBC.

- Моментальный снимок типа записей — статические копию набора записей, которые можно использовать для поиска данных и создания отчетов. Объект типа **набора записей** может содержать поля из одного или нескольких таблиц в базе данных, но не могут быть обновлены. Этот тип соответствует статическим курсором ODBC.

- Прямого только для типа записей — аналогична моментальный снимок, за исключением того, что предоставляется не курсора. Можно выполнять только прокрутку вперед записей. Это повышает производительность в ситуациях, только чтобы сделать один проход в наборе результатов. Этот тип соответствует только вперед текущей позиции ODBC.

- Записей динамического типа — результатов запроса изменять из одного или нескольких базовые таблицы, в которых можно добавить, изменения или удаления записей из возвращающие строки запроса. Более того другим пользователям добавление, удаление или изменение в базовые таблицы также отображаются записи в наборе **записей**. Этот тип соответствует динамического курсора ODBC (только для рабочих областей технология ODBCDirect).

> [!NOTE]
> Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.

Можно выбрать тип объекта **набора записей** , которые необходимо создать с помощью метода **OpenRecordset** аргумент типа.

В рабочей области Microsoft Access Если не указать тип DAO предпринимается попытка создать тип **набора записей** с большинство функциональных возможностей, начиная с таблицей. Если этот тип не поддерживается, DAO пытается подмножества, а затем моментальный снимок и, наконец, однонаправленные тип объекта **набора записей** .

В рабочей области технология ODBCDirect Если не указать тип DAO пытается создать тип **набора записей** с быстрый ответ на запрос, начиная с последовательного доступа. Если этот тип не поддерживается, DAO пытается моментальный снимок, а затем подмножества и, наконец, объект **набора записей** динамического типа.

При создании объекта **набора записей** с помощью объекта **[TableDef](tabledef-object-dao.md)** несвязанных в рабочей области Microsoft Access, создаются в таблице объекты **набора записей** . С помощью связанных таблиц и таблиц в базах данных ODBC engine подключенной базы данных Microsoft Access можно создавать только динамического или объектов **наборов записей** типа снимка.

Новый объект **набора записей** автоматически добавляется в коллекцию **наборов записей** при открытии объекта и автоматически удаляются при закрытии.

> [!NOTE]
> Если использовать переменные для представления объекта **набора записей** и объекта **базы данных** , содержащее **набор записей**, убедитесь, что переменные иметь те же области или время жизни. Например если объявить открытую переменную, которая представляет собой объект- **записей** , убедитесь, что переменной, которая представляет базе **базы данных** , содержащий **записей** также общедоступный или объявляется в **Sub** или **Function** процедуры, с помощью ключевое слово **Static** .

Можно создать любое количество переменных объекта **набора записей** при необходимости. Объекты различных **наборов записей** можно получить доступ к таблиц, запросов и полей без конфликтов.

Динамический набор – моментальный снимок – и прямого — только — тип объектов **наборов записей** хранятся в локальной памяти. Если в локальной памяти для хранения данных, не хватает места, ядро базы данных Microsoft Access сохраняет дополнительные данные во ВРЕМЕННЫЙ дискового пространства. Если исчерпано этого пространства, то перехватываемые возникает ошибка.

По умолчанию коллекции объекта **набора записей** представляет коллекцию **полей** , а свойство **[Value](field-value-property-dao.md)** является свойством по умолчанию объекта **[поля](field-object-dao.md)** . Используйте эти значения по умолчанию для упрощения кода.

При создании объекта **набора записей** текущей записи располагается первой записи при наличии записей. Если нет записей, **RecordCount** свойство имеет значение 0, а также ** **BOF** или **EOF** параметров выполняются**.

**MoveNext**, **MovePrevious**, **MoveFirst**и **MoveLast** методы можно использовать для изменения положения текущей записи. Объекты **набора записей** прямого — только — тип поддерживает только метод **MoveNext** . При использовании методов перемещения посетите каждая запись (или «рассмотрение» **набора записей**), можно использовать свойства **BOF** и **EOF** на наличие начала или окончания объекта **набора записей** .

С и моментальный снимок добавляющий объектов **наборов записей** в рабочую область для Microsoft Access, можно также использовать методы поиска, такие как **FindFirst**поиск определенной записи на основе критериев. Если запись не найден, свойство **NoMatch** имеет значение **True**. Объектам-таблица тип **набора записей** для проверки записей с помощью метода **Seek** .

Свойство **Type** указывает тип объекта **Recordset** , созданного и свойство **с возможностью записи** указывает, можно ли изменить записи объекта.

Сведения о структуре базовая таблица, таких как имена и типы данных каждого объекта **поля** и любые объекты **индекса** хранится в объекте **TableDef** .

Для ссылки на объект **набора записей** в коллекции по его порядковый номер или по **его свойства Name** , используйте любой из следующих форм синтаксиса:

- **Наборы записей** (0)

- **Наборы записей** («имя»)

- **Наборы записей**\!\[имя\]

> [!NOTE]
> Объект **набора записей** можно открыть из одного источника данных или базы данных более одного раза, Создание повторяющихся имен в коллекции **наборов записей** . Следует назначить объектов **наборов записей** объектных переменных и обращаться к ним с именем переменной.

## <a name="example"></a>Пример

В этом примере демонстрируется **набора записей** объекты и коллекции **наборов записей** , открыв четыре различных типов **наборов записей**, перечисления коллекции наборов записей текущей **базы данных**и перечисление ** Свойства** коллекцию каждого **набора записей**.

```vb
    Sub RecordsetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstTable As Recordset 
       Dim rstDynaset As Recordset 
       Dim rstSnapshot As Recordset 
       Dim rstForwardOnly As Recordset 
       Dim rstLoop As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
     
          ' Open one of each type of Recordset object. 
          Set rstTable = .OpenRecordset("Categories", _ 
             dbOpenTable) 
          Set rstDynaset = .OpenRecordset("Employees", _ 
             dbOpenDynaset) 
          Set rstSnapshot = .OpenRecordset("Shippers", _ 
             dbOpenSnapshot) 
          Set rstForwardOnly = .OpenRecordset _  
             ("Employees", dbOpenForwardOnly) 
     
          Debug.Print "Recordsets in Recordsets " & _ 
             "collection of dbsNorthwind" 
     
          ' Enumerate Recordsets collection. 
          For Each rstLoop In .Recordsets 
     
             With rstLoop 
                Debug.Print "  " & .Name 
     
                ' Enumerate Properties collection of each 
                ' Recordset object. Trap for any  
                ' properties whose values are invalid in  
                ' this context. 
                For Each prpLoop In .Properties 
                   On Error Resume Next 
                   If prpLoop <> "" Then Debug.Print _ 
                      "    " & prpLoop.Name & _ 
                      " = " & prpLoop 
                   On Error GoTo 0 
                Next prpLoop 
     
             End With 
     
          Next rstLoop 
     
          rstTable.Close 
          rstDynaset.Close 
          rstSnapshot.Close 
          rstForwardOnly.Close 
     
          .Close 
       End With 
     
    End Sub 
```

<br/>

В этом примере используется метод **OpenRecordset** Открытие пять разных объектов **набора записей** и отображения их содержимого. Процедура OpenRecordsetOutput является обязательным для выполнения этой процедуры.

```vb
    Sub OpenRecordsetX() 
     
       Dim wrkAcc As Workspace 
       Dim wrkODBC As Workspace 
       Dim dbsNorthwind As Database 
       Dim conPubs As Connection 
       Dim rstTemp As Recordset 
       Dim rstTemp2 As Recordset 
     
       ' Open Microsoft Access and ODBCDirect workspaces, Microsoft  
       ' Access database, and ODBCDirect connection. 
       Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
       Set wrkODBC = CreateWorkspace("", "admin", "", dbUseODBC) 
       Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
        
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       Set conPubs = wrkODBC.OpenConnection("", , , _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
     
       ' Open five different Recordset objects and display the  
       ' contents of each. 
     
       Debug.Print "Opening forward-only-type recordset " & _ 
          "where the source is a QueryDef object..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "Ten Most Expensive Products", dbOpenForwardOnly) 
       OpenRecordsetOutput rstTemp 
     
       Debug.Print "Opening read-only dynaset-type " & _ 
          "recordset where the source is an SQL statement..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "SELECT * FROM Employees", dbOpenDynaset, dbReadOnly) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the Filter property to retrieve only certain  
       ' records with the next OpenRecordset call. 
       Debug.Print "Opening recordset from existing " & _ 
          "Recordset object to filter records..." 
       rstTemp.Filter = "LastName >= 'M'" 
       Set rstTemp2 = rstTemp.OpenRecordset() 
       OpenRecordsetOutput rstTemp2 
     
       Debug.Print "Opening dynamic-type recordset from " & _ 
          "an ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset( _ 
          "SELECT * FROM stores", dbOpenDynamic) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the StillExecuting property to determine when the  
       ' Recordset is ready for manipulation. 
       Debug.Print "Opening snapshot-type recordset based " & _ 
          "on asynchronous query to ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset("publishers", _ 
          dbOpenSnapshot, dbRunAsync) 
       Do While rstTemp.StillExecuting 
          Debug.Print "  [still executing...]" 
       Loop 
       OpenRecordsetOutput rstTemp 
     
       rstTemp.Close 
       dbsNorthwind.Close 
       conPubs.Close 
       wrkAcc.Close 
       wrkODBC.Close 
     
    End Sub 
     
    Sub OpenRecordsetOutput(rstOutput As Recordset) 
     
       ' Enumerate the specified Recordset object. 
       With rstOutput 
          Do While Not .EOF 
             Debug.Print , .Fields(0), .Fields(1) 
             .MoveNext 
          Loop 
       End With 
     
    End Sub 
```

<br/>

В этом примере открывает объект **набора записей** динамического типа и перечисление ее записи.

```vb
    Sub dbOpenDynamicX() 
     
       Dim wrkMain As Workspace 
       Dim conMain As Connection 
       Dim qdfTemp As QueryDef 
       Dim rstTemp As Recordset 
       Dim strSQL As String 
       Dim intLoop As Integer 
     
       ' Create ODBC workspace and open connection to 
       ' SQL Server database. 
       Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
          "admin", "", dbUseODBC) 
           
       ' Note: The DSN referenced below must be configured to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server.     
       Set conMain = wrkMain.OpenConnection("Publishers", _ 
          dbDriverNoPrompt, False, _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
           
       ' Open dynamic-type recordset. 
       Set rstTemp = _ 
          conMain.OpenRecordset("authors", _ 
          dbOpenDynamic) 
     
       With rstTemp 
          Debug.Print "Dynamic-type recordset: " & .Name 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !au_lname & ", " & _ 
                !au_fname 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       conMain.Close 
       wrkMain.Close 
     
    End Sub 
```

<br/>

В этом примере открывается типа динамического **набора записей** и показывает область, к которому его поля, обновляемых.

```vb
    Sub dbOpenDynasetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstInvoices As Recordset 
       Dim fldLoop As Field 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstInvoices = _ 
          dbsNorthwind.OpenRecordset("Invoices", dbOpenDynaset) 
     
       With rstInvoices 
          Debug.Print "Dynaset-type recordset: " & .Name 
     
          If .Updatable Then 
             Debug.Print "  Updatable fields:" 
     
             ' Enumerate Fields collection of dynaset-type 
             ' Recordset object, print only updatable 
             ' fields. 
             For Each fldLoop In .Fields 
                If fldLoop.DataUpdatable Then 
                   Debug.Print "    " & fldLoop.Name 
                End If 
             Next fldLoop 
     
          End If 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

В этом примере открывается прямого только для типа **записей**, показывает, характеристики его только для чтения и шаги по **набора записей** с помощью метода **MoveNext** .

```vb 
Sub dbOpenForwardOnlyX() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim fldLoop As Field 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   ' Open a forward-only-type Recordset object. Only the  
   ' MoveNext and Move methods may be used to navigate  
   ' through the recordset. 
   Set rstEmployees = _ 
      dbsNorthwind.OpenRecordset("Employees", _ 
      dbOpenForwardOnly) 
 
   With rstEmployees 
      Debug.Print "Forward-only-type recordset: " & _ 
         .Name & ", Updatable = " & .Updatable 
 
      Debug.Print "  Field - DataUpdatable" 
      ' Enumerate Fields collection, printing the Name and  
      ' DataUpdatable properties of each Field object. 
      For Each fldLoop In .Fields 
         Debug.Print "    " & _ 
            fldLoop.Name & " - " & fldLoop.DataUpdatable 
      Next fldLoop 
 
      Debug.Print "  Data" 
      ' Enumerate the recordset. 
      Do While Not .EOF 
         Debug.Print "    " & !FirstName & " " & _ 
            !LastName 
         .MoveNext 
      Loop 
 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
```

<br/>

В этом примере открывается типа **записей** и демонстрируются характеристики его только для чтения.

```vb
    Sub dbOpenSnapshotX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          Debug.Print "Snapshot-type recordset: " & _ 
             .Name 
     
          ' Enumerate the Properties collection of the 
          ' snapshot-type Recordset object, trapping for 
          ' any properties whose values are invalid in  
          ' this context. 
          For Each prpLoop In .Properties 
             On Error Resume Next 
             Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
             On Error Goto 0 
          Next prpLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

В этом примере открывается таблица тип **набора записей**, задает его свойства **Index** и перечисляет его записей.

```vb
    Sub dbOpenTableX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' dbOpenTable is default. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
     
       With rstEmployees 
          Debug.Print "Table-type recordset: " & .Name 
     
          ' Use predefined index. 
          .Index = "LastName" 
          Debug.Print "  Index = " & .Index 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !LastName & ", " & _ 
                !FirstName 
             .MoveNext 
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

<br/>

Следующем примере показано, как открыть записей, основанный на параметр запроса.

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

Следующем примере показано, как открыть набор записей на основе таблицы или запроса.

```vb
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

Следующем примере показано, как открыть записей, на основе инструкции структурированный язык запросов (SQL).

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

Следующем примере показано, как использовать методы FindFirst и FindNext для поиска записей в наборе записей.

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```

<br/>

Следующем примере показано, как скопировать результаты запроса на лист в новой книги Microsoft Excel.

```vb
    Public Sub CopyDataFromQuery( _
        xlApp As Excel.Application, _
        strQueryName As String)
    
        ' If the xlApp object exists
        If Not xlApp Is Nothing Then
        
            ' If the Workbook exists
            If xlApp.Workbooks.Count = 1 Then
            
                ' Create Recrodset Object from the Query
                Dim rsQuery As DAO.Recordset
                Set rsQuery = Application.CurrentDb.OpenRecordset(strQueryName)
                
                ' Get the Cells object
                Dim Cells As Object
                Set Cells = xlApp.Workbooks(1).ActiveSheet.Cells
                
                ' Copy the Data from the Query into the Sheet
                Cells.CopyFromRecordset rsQuery
                
            End If
        End If
    
    End Sub
```

