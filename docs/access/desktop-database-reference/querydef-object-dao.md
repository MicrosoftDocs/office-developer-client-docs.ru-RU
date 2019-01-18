---
title: Объект QueryDef (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a94d34a2dbe8043e6db637b649f59047cf3f1dda
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713557"
---
# <a name="querydef-object-dao"></a>Объект QueryDef (DAO)

**Применимо к:** Access 2013 | Office 2013 

Объект **QueryDef** — сохраненных определение запроса в базе данных ядра базы данных Microsoft Access.

## <a name="remarks"></a>Замечания

Чтобы определить запрос, можно использовать объекта **QueryDef** . Например можно выполнить следующие действия.

- Используйте свойство **SQL** или возвращает определение запроса.

- Используйте коллекцию **параметров** объекта **QueryDef** или возвращает параметры запроса.

- Свойство **типа** возвращает значение, указывающее ли запрос выбирает записи из существующей таблицы, создает новую таблицу, вставляет записей из одной таблицы в другой таблице, удаляет записи или обновления записей.

- Свойство **MaxRecords** максимальное число записей, возвращаемых запросом.

- Чтобы указать, как долго ждать, пока запрос возвращает записи, воспользуйтесь свойством **время ожидания ODBC** . **Время ожидания ODBC** свойство применяется для любого запроса, который получает доступ к данным ODBC.

- Свойство **ReturnsRecords** служит для указания, что запрос возвращает записи. Свойство **ReturnsRecords** допустимо только на запросы к серверу.

- Используйте свойство **Подключить** базу данных ODC для выполнения запроса к серверу.

Можно также создать временные объекты **QueryDef** . В отличие от постоянных объектов **QueryDef** временные объекты **QueryDef** не на жестком диске или в коллекцию **QueryDefs** . Временные объекты **QueryDef** полезны для запросов, которые необходимо выполнить несколько раз во время выполнения, но не не нужно сохранить на диске, особенно в том случае, если вы создаете их инструкции SQL во время выполнения.

Постоянное объекта **QueryDef** в рабочей области Microsoft Access можно считать скомпилированной инструкции SQL. При выполнении запроса из основного объекта **QueryDef** запрос будет выполняться быстрее, чем при запуске эквивалентный оператор SQL из метода **OpenRecordset** . Это, поскольку ядро базы данных Microsoft Access не нужно компиляции, перед его выполнением.

Рекомендуемый способ использовать собственный диалект SQL внешних СУБД, через ядро базы данных Microsoft Access — через объекты **QueryDef** . Например можно создать запрос Microsoft SQL Server и сохраните ее в объекте **QueryDef** . При необходимости использовать запрос SQL ядра базы данных Microsoft Access необходимо указать строку свойства **подключения** , указывающий на внешнем источнике данных. Запросы с допустимого свойства **подключения** обхода ядро базы данных Microsoft Access и передает запрос непосредственно к серверу внешние базы данных для использования.

Чтобы создать новый объект **QueryDef** , используйте метод **CreateQueryDef** . В рабочей области Microsoft Access Если указать строку для аргумента имени или явно задать свойство **Name** нового объекта **QueryDef** не – пустую строку будет создать постоянное **QueryDef** , который будет автоматически в коллекцию **QueryDefs** и на жестком диске. Временные объекта **QueryDef** приведет к передав строку нулевой длины в качестве аргумента имя и явно установки свойства **Name** в строку нулевой длины.

Для ссылки на объект **QueryDef** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:

QueryDefs(0)

QueryDefs("name")

QueryDefs\! \[ имя\]

Можно ссылаться на временные объекты **QueryDef** только с объектных переменных, назначенных им.

**Автор ссылку** [UtterAccess](https://www.utteraccess.com) сообщества. UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.

- [Запросы: Документ SQL в Word](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a>Пример

В этом примере создается новый объект **QueryDef** и добавляет его в коллекцию **QueryDefs** объекта данных Northwind **базы данных** . Затем выполняется перечисление коллекции **QueryDefs** и коллекции **свойств** нового **QueryDef**.

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

В этом примере используется метод **CreateQueryDef** для создания и выполнения временное и постоянное **QueryDef**. Функция GetrstTemp является обязательным для выполнения этой процедуры.

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

Следующем примере показано, как заменить оператор структурированный язык запросов (SQL) в сохраненный запрос.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    ‘To change the Where clause in a saved query  
    Dim qdf as QueryDef
    Dim db as Database
    Set db = CurrentDB
    Set qdf = db.QueryDefs("YourQueryName")
    qdf.SQL = ReplaceWhereClause(qdf.SQL, strYourNewWhereClause)
    set qdf = Nothing
    set db = Nothing
    
    Public Function ReplaceWhereClause(strSQL As Variant, strNewWHERE As Variant)
    On Error GoTo Error_Handler
    
    ‘This subroutine accepts a valid SQL string and Where clause, and
    ‘returns the same SQL statement with the original Where clause (if any)
    ‘replaced by the passed in Where clause.
    ‘
    ‘INPUT:
    ‘ strSQL valid SQL string to change
    ‘OUTPUT:
    ‘ strNewWHERE New WHERE clause to insert into SQL statement
    ‘
        Dim strSELECT As String, strWhere As String
        Dim strOrderBy As String, strGROUPBY As String, strHAVING As String
    
        Call ParseSQL(strSQL, strSELECT, strWhere, strOrderBy, _
            strGROUPBY, strHAVING)
    
        ReplaceWhereClause = strSELECT &""& strNewWHERE &""_
            & strGROUPBY &""& strHAVING &""& strOrderBy
    
        Exit_Procedure:
            Exit Function
    
        Error_Handler:
            MsgBox (Err.Number & ": " & Err.Description)
            Resume Exit_Procedure
    
    End Function
```

