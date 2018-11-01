---
title: Database.CreateQueryDef Method (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 24cb363d253e9abd18d251299c36edbdb371d56d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880784"
---
# <a name="databasecreatequerydef-method-dao"></a>Database.CreateQueryDef Method (DAO)

**Применимо к**: Access 2013, Office 2013

Создает новый объект **[QueryDef](querydef-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . CreateQueryDef (***имя***, ***SQLText***)

*выражение* Переменная, которая представляет собой объект **базы данных** .

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
<td><p>Имя</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>String</strong> подтип), уникальным образом новые <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p>SQLText</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>String</strong> подтип), которая является инструкцией SQL, определение <strong>QueryDef</strong>. Если опустить аргумент, можно определить <strong>QueryDef</strong> путем установки свойства <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> до или после добавления его в коллекцию.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

QueryDef

## <a name="remarks"></a>Замечания

В рабочей области Microsoft Access Если вы укажите отличное от строку нулевой длины имени при создании **QueryDef**результирующего объекта **QueryDef** автоматически добавляется к коллекции **[QueryDefs](querydefs-collection-dao.md)** .

Если объектом, заданным с именем уже должна быть членом **QueryDefs** коллекции, возникает ошибка времени выполнения. Временные **QueryDef** можно создать с помощью строку нулевой длины для аргумента имени, при выполнении метода **CreateQueryDef** . Это также можно сделать, задав свойство **[Name](querydef-name-property-dao.md)** только что созданный **QueryDef** в строку нулевой длины (»»). 

Временные объекты **QueryDef** полезны, если требуется повторно использовать динамические инструкции SQL, не создавая для создания новых постоянных объектов в коллекции **QueryDefs** . Временные **QueryDef** невозможно добавить в любой коллекции, так как строку нулевой длины не является допустимым именем для постоянного объекта **QueryDef** . Всегда можно задать **имя** и свойства **SQL** объекта **QueryDef** только что созданный и затем добавьте **QueryDef** в коллекцию **QueryDefs** .

Чтобы запустить инструкции SQL в объект **QueryDef** , используйте метод **[Execute](querydef-execute-method-dao.md)** или **[OpenRecordset](database-openrecordset-method-dao.md)** .

С помощью объекта **QueryDef** является предпочтительным для выполнения запросов к серверу с использованием баз данных ODBC.

Для удаления объекта **QueryDef** из коллекции **QueryDefs** в базе данных ядра базы данных Microsoft Access, используйте метод **[Delete](querydefs-delete-method-dao.md)** в семействе сайтов.

## <a name="example"></a>Пример

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

В этом примере использует **CreateQueryDef** и **OpenRecordset** методы и свойства **SQL** для запроса к таблице заголовки в образце базы данных Pubs Microsoft SQL Server и вернуть название и идентификатор заголовка лидера продаж. Затем запрашивает таблицы авторов и указывает на отправку выполняется проверка премии каждого автора на его основе или совместно использовать свой прямые (общее вознаграждение равно 1000 долларов США и каждого автора должны принимать процент это значение).

```vb 
Sub ClientServerX2() 
 
   Dim dbsCurrent As Database 
   Dim qdfBestSellers As QueryDef 
   Dim qdfBonusEarners As QueryDef 
   Dim rstTopSeller As Recordset 
   Dim rstBonusRecipients As Recordset 
   Dim strAuthorList As String 
 
   ' Open a database from which QueryDef objects can be  
   ' created. 
   Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
   ' Create a temporary QueryDef object to retrieve 
   ' data from a Microsoft SQL Server database. 
   Set qdfBestSellers = dbsCurrent.CreateQueryDef("") 
   With qdfBestSellers 
      ' Note: The DSN referenced below must be configured to  
      '       use Microsoft Windows NT Authentication Mode to  
      '       authorize user access to the Microsoft SQL Server. 
      .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
      .SQL = "SELECT title, title_id FROM titles " & _ 
         "ORDER BY ytd_sales DESC" 
      Set rstTopSeller = .OpenRecordset() 
      rstTopSeller.MoveFirst 
   End With 
 
   ' Create a temporary QueryDef to retrieve data from 
   ' a Microsoft SQL Server database based on the results from 
   ' the first query. 
   Set qdfBonusEarners = dbsCurrent.CreateQueryDef("") 
   With qdfBonusEarners 
      ' Note: The DSN referenced below must be configured to  
      '       use Microsoft Windows NT Authentication Mode to  
      '       authorize user access to the Microsoft SQL Server. 
      .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
      .SQL = "SELECT * FROM titleauthor " & _ 
         "WHERE title_id = '" & _ 
         rstTopSeller!title_id & "'" 
      Set rstBonusRecipients = .OpenRecordset() 
   End With 
 
   ' Build the output string. 
   With rstBonusRecipients 
      Do While Not .EOF 
         strAuthorList = strAuthorList & "  " & _ 
            !au_id & ":  $" & (10 * !royaltyper) & vbCr 
         .MoveNext 
      Loop 
   End With 
 
   ' Display results. 
   MsgBox "Please send a check to the following " & _ 
      "authors in the amounts shown:" & vbCr & _ 
      strAuthorList & "for outstanding sales of " & _ 
      rstTopSeller!Title & "." 
 
   rstTopSeller.Close 
   dbsCurrent.Close 
 
End Sub 
```

<br/>

Следующий пример демонстрирует создание запроса с параметрами. Запрос с именем **myQuery** создается с двумя параметрами, с именем Param1 и Param2. Для этого свойства SQL запроса значение оператор структурированный язык запросов (SQL), который определяет параметры.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```
