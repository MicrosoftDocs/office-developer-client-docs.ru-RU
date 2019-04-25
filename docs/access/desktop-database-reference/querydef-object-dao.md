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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301059"
---
# <a name="querydef-object-dao"></a>Объект QueryDef (DAO)

**Область применения**: Access 2013 | Office 2013 

Объект **QueryDef** — это сохраняемое определение запроса в базе данных ядра СУБД Microsoft Access.

## <a name="remarks"></a>Примечания

Объект **QueryDef** можно использовать для определения запроса. Например, вы можете:

- Использовать свойство **SQL**, чтобы задать или вернуть определение запроса.

- Использовать коллекцию **Parameters** объекта **QueryDef**, чтобы задать или вернуть параметры запроса.

- Использовать свойство **Type**, чтобы вернуть значение, которое указывает действие запроса: выбор записей из существующей таблицы, создание таблицы, вставка записей из одной таблицы в другую, удаление записей или обновление записей.

- Использовать свойство **MaxRecords**, чтобы ограничить число записей, возвращаемых запросом.

- Использовать свойство **ODBCTimeout**, чтобы указать длительность ожидания перед возвращением запросом записей. Свойство **ODBCTimeout** применяется к любому запросу, обращающемуся к данным ODBC.

- Использовать свойство **ReturnsRecords**, чтобы указать, что запрос возвращает записи. Применение свойства **ReturnsRecords** допустимо только для запросов SQL к серверу.

- Использовать свойство **Connect**, чтобы создать запрос SQL к серверу для базы данных ODC.

Также можно создавать временные объекты **QueryDef**. В отличие от постоянных объектов **QueryDef** временные объекты **QueryDef** не сохраняются на диске и не добавляются в коллекцию **QueryDefs**. Временные объекты **QueryDef** удобно использовать для запросов, которые нужно неоднократно запускать во время выполнения, но не требуется сохранять на диск, в частности, если создаются их инструкции SQL во время выполнения.

Постоянный объект **QueryDef** в рабочей области Microsoft Access можно рассматривать как скомпилированную инструкцию SQL. Если запрос запускается из постоянного объекта **QueryDef**, он выполняется быстрее, чем при запуске эквивалентной инструкции SQL с помощью метода **OpenRecordset**. Это объясняется тем, что ядру СУБД Microsoft Access не нужно компилировать запрос перед его выполнением.

Предпочтительный способ использования диалекта SQL внешнего ядра СУБД с доступом через ядро СУБД Microsoft Access состоит в применении объектов **QueryDef**. Например, можно создать запрос Microsoft SQL Server и сохранить его в объекте **QueryDef**. Если нужно использовать запрос SQL не на основе ядра СУБД Microsoft Access, потребуется предоставить строку свойства **Connect**, указывающую на внешний источник данных. Запросы с допустимыми свойствами **Connect** обходят ядро СУБД Microsoft Access и передаются непосредственно к серверу внешней базы данных для обработки.

Чтобы создать новый объект **QueryDef**, используйте метод **CreateQueryDef**. В рабочей области Microsoft Access, если указать строку для аргумента имени или явно задать строку ненулевой длины в качестве значения свойства **Name** нового объекта **QueryDef**, будет создан постоянный объект **QueryDef**, который будет автоматически добавлен в коллекцию **QueryDefs** и сохранен на диске. Если указать строку ненулевой длины в качестве аргумента имени или явно задать строку нулевой длины в качестве значения свойства **Name**, будет создан временный объект **QueryDef**.

Чтобы сослаться на объект **QueryDef** в коллекции по его порядковому номеру или по его свойству **Name**, используйте любую из указанных ниже синтаксических форм.

QueryDefs(0)

QueryDefs("name")

QueryDefs\!\[ name\]

Ссылаться на временные объекты **QueryDef** можно только по назначенным им объектным переменным.

**Ссылка, предоставляемая** сообществом [UtterAccess](https://www.utteraccess.com). UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.

- [Запросы: документирование SQL в Word](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a>Пример

В этом примере создается новый объект **QueryDef**, который добавляется в коллекцию **QueryDefs** объекта **Database** компании Northwind. Затем выполняется перечисление коллекции **QueryDefs** и коллекции **Properties** нового объекта **QueryDef**.

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

В этом примере используется метод **CreateQueryDef**, чтобы создать и выполнить временный и постоянный объекты **QueryDef**. Функция GetrstTemp необходима для запуска этой процедуры.

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

В следующем примере показано, как заменить инструкцию SQL в сохраненном запросе.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

