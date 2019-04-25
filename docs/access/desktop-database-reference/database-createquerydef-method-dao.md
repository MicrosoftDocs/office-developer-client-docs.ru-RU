---
title: Метод Database.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c19ef8ab8ef2e937ba7467b3695f9aa5780c21c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294983"
---
# <a name="databasecreatequerydef-method-dao"></a>Метод Database.CreateQueryDef (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*expression* .CreateQueryDef(***Name***, ***SQLText***)

*выражение*: переменная, представляющая объект **Database**.

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
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Необязательно заполнять.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Объект типа <strong>Variant</strong> (подтип <strong>String</strong>), однозначно определяющий новый объект <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Объект <strong>Variant</strong> (подтип <strong>String</strong>), представляющий инструкцию SQL, которая определяет объект <strong>QueryDef</strong>. Если не указать этот аргумент, вы можете определить объект <strong>QueryDef</strong>, задав его свойство <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> до или после его добавления к коллекции.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

QueryDef

## <a name="remarks"></a>Примечания

В рабочей области Microsoft Access, если указать в качестве имени какое-либо значение, кроме строки нулевой длины, при создании объекта **QueryDef**, полученный объект **QueryDef** будет автоматически добавлен к коллекции **[QueryDefs](querydefs-collection-dao.md)**.

Если объект, указанный по имени, уже является элементом коллекции **QueryDefs**, возникает ошибка во время выполнения. Вы можете создать временный объект **QueryDef**, указав в качестве имени строку нулевой длины при выполнении метода **CreateQueryDef**. Это также можно сделать, указав строку нулевой длины ("") в качестве значения свойства **[Name](querydef-name-property-dao.md)** нового объекта **QueryDef**. 

Временные объекты **QueryDef** полезны, если требуется регулярно использовать динамические инструкции SQL, не создавая постоянных объектов в коллекции **QueryDefs**. Временный объект **QueryDef** невозможно добавить к какой-либо коллекции, так как строка нулевой длины не является допустимым именем постоянного объекта **QueryDef**. Вы всегда можете задать свойства **Name** и **SQL** нового объекта **QueryDef**, а затем добавить объект **QueryDef** к коллекции **QueryDefs**.

Чтобы выполнить инструкцию SQL в объекте **QueryDef**, используйте метод **[Execute](querydef-execute-method-dao.md)** или **[OpenRecordset](database-openrecordset-method-dao.md)**.

Использование объекта **QueryDef** является предпочтительным способом выполнения SQL-запросов к серверу с базами данных ODBC.

Чтобы удалить объект **QueryDef** из коллекции **QueryDefs** в базе данных ядра СУБД Microsoft Access, используйте метод **[Delete](querydefs-delete-method-dao.md)** для этой коллекции.

## <a name="example"></a>Пример

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

В этом примере используются методы **CreateQueryDef** и **OpenRecordset**, а также свойство **SQL**, чтобы отправить запрос к таблице названий в примере базы данных Pubs из Microsoft SQL Server и получить название самой продаваемой книги, а также его идентификатор. Затем этот пример отправляет запрос к таблице авторов и предлагает пользователю отправить премиальный чек каждому автору с учетом доли его лицензионных выплат (общая сумма премии составляет 1000 долл. США, а каждый автор должен получить определенный процент от этой суммы).

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

В приведенном ниже примере показано, как создать запрос с параметрами. Запрос с именем **myQuery** создается с двумя параметрами: Param1 и Param2. Для этого в качестве свойства SQL запроса задается инструкция языка SQL, определяющая параметры.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
