---
title: Объект Recordset (DAO)
TOCTitle: Recordset Object
ms:assetid: 9774232c-e6da-175b-fc7f-ed2ab7908fa0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197799(v=office.15)
ms:contentKeyID: 48546469
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 19999159f7987be87031f88d1eec87980585f369
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284520"
---
# <a name="recordset-object-dao"></a>Объект Recordset (DAO)

**Применяется для:** Access 2013, Office 2013

Объект **Recordset** представляет записи в базовой таблице или записи, получаемые в результате выполнения запросов.

## <a name="remarks"></a>Комментарии

Вы можете использовать **Recordset**, чтобы управлять данными в базе данных на уровне записей. Если вы используете интерфейс DAO, вы можете управлять данными практически полностью с помощью объектов **Recordset**. Все объекты **Recordset** построены с использованием записей (строки) и полей (столбцы). Существует пять типов объектов **Recordset**:

- Объект Recordset табличного типа — представление в коде базовой таблицы, которое вы можете использовать для добавления, изменения и удаления записей из таблицы одной базы данных (только для рабочей области Microsoft Access).

- Объект Recordset типа Dynaset — результат запроса, который может обновлять записи. Объект **Recordset** типа Dynaset является динамическим набором записей, которые можно использовать для добавления, изменения и удаления записей из базовой таблицы базы данных или таблиц. Объект **Recordset** типа Dynaset может содержать поля из одной или нескольких таблиц в базе данных. Этот тип соответствует курсору набор ключей ODBC.

- Объект Recordset типа моментальный снимок — статическая копия набора записей, которую можно использовать для поиска данных или создания отчетов. Объект **Recordset** типа моментальный снимок может содержать поля из одной или нескольких таблиц в базе данных, но не может обновляться. Этот тип соответствует статическому курсору ODBC.

- Объект Recordset однонаправленного типа — аналогичен моментальному снимку с единственной разницей в отсутствии курсора. Вы можете только прокручивать записи вперед. Это повышает производительность в ситуациях, где достаточно только один раз просмотреть итоговый набор. Этот тип соответствует однонаправленному курсору ODBC.

- Динамический тип объекта Recordset — набор результатов запроса, получаемый из одной или нескольких базовых таблиц, в котором вы можете добавить, изменить или удалить записи из возвращающего строку запроса. Кроме того, записи, которые добавляют, удаляют или изменяют другие пользователи в базовой таблице, также будут отображаться в вашем объекте **Recordset**. Этот тип соответствует динамическому курсору ODBC (только для рабочих областей ODBCDirect).

> [!NOTE]
> Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.

Вы можете выбрать тип объекта **Recordset**, который вы хотите создать, с помощью аргумента типа метода **OpenRecordset**.

В рабочей области Microsoft Access, если не задан тип, интерфейс DAO пытается создать тип объекта**Recordset** с наиболее широким набором функций, начиная с табличного. Если этот тип не поддерживается, интерфейс DAO пытается создать объект типа Dynaset, затем моментальный снимок и, наконец, однонаправленный тип объекта **Recordset**.

В рабочей области ODBCDirect, если не задан тип, интерфейс DAO пытается создать тип объекта**Recordset** с самой быстрой реакцией на запрос, начиная с однонаправленного типа. Если этот тип не поддерживается, интерфейс DAO пытается создать объект типа мгновенный снимок, затем dynaset и, наконец, динамический тип объекта **Recordset**.

При создании объекта **Recordset** с помощью несвязанного объекта ** [TableDef](tabledef-object-dao.md) ** в рабочей области Microsoft Access, создается табличный тип объекта **Recordset**. Только объекты **Recordset** динамического типа или типа моментальный снимок могут создаваться со связанными таблицами или таблицами в базах данных ODBC с подключенным ядром СУБД Microsoft Access.

Объект **Recordset** автоматически добавляется в коллекцию **Recordsets** при открытии объекта и автоматически удаляется при его закрытии.

> [!NOTE]
> Если вы используете переменные для представления объекта **Recordset** и объекта **Database**, который содержит объект **Recordset**, убедитесь, что переменные принадлежат к той же области или имеют то же время существования. Например, если вы объявляете публичную переменную, которая определяет объект **Recordset**, убедитесь, что переменная, которая представляет **Database** с **Recordset**, также является публичной, или объявлена с помощью процедуры **Sub** или **Function** с применением ключевого слова **Static**.

Вы можете создать любое количество переменных объекта **Recordset** при необходимости. Различные объекты **Recordset** могут получать доступ к одним таблицам, запросам и полям без возникновения конфликта.

Типы Dynaset, моментальный снимок и однонаправленный для объекта **Recordset** хранятся в локальной памяти. Если в локальной памяти для хранения данных недостаточно места, ядро СУБД Microsoft Access сохраняет дополнительные данные в дисковом пространстве TEMP. Если свободное место заканчивается, возникает перехватываемая ошибка.

По умолчанию для объекта **Recordset** используется коллекция **Поля**, а используемым по умолчанию свойством объекта ** [Поле](field-object-dao.md) ** является свойство** [Значение](field-value-property-dao.md) **. Используйте эти настройки по умолчанию для упрощения вашего кода.

При создании объекта **Recordset** текущая запись расположена по направлению к первой записью, если есть какие-либо записи. Если записи отсутствуют, свойство **RecordCount** имеет значение 0, а свойство **BOF** и **EOF** имеют значение **ИСТИНА**.

Вы можете использовать методы **MoveNext**, **MovePrevious**, **MoveFirst** и **MoveLast**, чтобы изменить положение текущей записи. Объекты **Recordset** однонаправленного типа поддерживают только метод **MoveNext**. При использовании методов перемещения для перехода к каждой записи (или «прогулки» по объекту **Recordset**), вы можете использовать свойства **BOF** и **EOF**, чтобы проверить начало или конец объекта **Recordset**.

Для объектов **Recordset** типа dynaset и моментальный список в рабочей области Microsoft Access можно также использовать методы поиска, например **FindFirst**, чтобы найти определенную запись на основе критериев. Если запись не найдена, свойство **NoMatch** получает значение **ИСТИНА**. Для табличного типа объектов **Recordset** можно сканировать записи, используя метод **Seek**.

Свойство **Type** указывает тип созданного объекта **Recordset**, а свойство **Updatable** указывает на то, можете ли вы изменить записи объекта.

Сведения о структуре базовой таблицы, например, имена и типы данных каждого объекта **Field** и любых объектов **Index** хранятся в объекте **TableDef**.

Чтобы сослаться на объект **Recordset** в коллекции по его порядковому номеру или по его свойству**Name**, используйте любую из следующих синтаксических форм:

- **Recordsets**(0)

- **Recordsets**("name")

- **Recordsets**\!\[name\]

> [!NOTE]
> Вы можете открыть объект **Recordset** из одного источника данных или базы данных несколько раз, создавая дублирующие имена в коллекции **Recordsets**. Вы должны назначить объекты **Recordsets** для переменных объекта и ссылаться на них по имени переменной.

## <a name="example"></a>Пример

В этом примере показаны объекты **Recordset** и коллекция **Recordset ** с помощью открытия четырех разных типов **Recordsets**, перечисления коллекции Recordsets для текущего объекта **Database**и перечисления коллекции **Properties** для каждого объекта **Recordset**.

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

В этом примере используется метод**OpenRecordset** для открытия пяти разных объектов **Recordset** и отображения их содержимого. Процедура OpenRecordsetOutput является обязательной для запуска этой процедуры.

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

В этом примере открывается динамический тип объекта **Recordset** и перечисляются ее записи.

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

В этом примере открывается тип dynaset объекта **Recordset** и отображаются уровни обновления его полей.

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

В этом примере открывается однонаправленный тип объекта **Recordset**, демонстрируются характеристики только для чтения и пошаговые инструкции для объекта **Recordset** и метода **MoveNext**.

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

В этом примере открывается тип моментальный снимок объекта **Recordset** и демонстрируются характеристики только для чтения.

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

В этом примере открывается табличный тип объекта **Recordset**, задается его свойство **Index** и перечисляются его записи.

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

<br/>

В приведенном ниже примере показано, как открыть объект Recordset на основании запроса параметра.

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

В приведенном ниже примере показано, как открыть объект Recordset на основании таблицы или запроса.

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

В приведенном ниже примере показано, как открыть объект Recordset на основании SQL оператора.

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

В приведенном ниже примере показано, как использовать методы FindFirst и FindNext для поиска записи в Recordset.

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

В приведенном ниже примере показано, как скопировать результаты запроса на лист в новой книге Microsoft Excel.

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

