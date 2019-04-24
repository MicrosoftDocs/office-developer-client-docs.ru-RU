---
title: Объект TableDef (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6e1182427c688e7c8b5ca53c1f5f4bb208b3609a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308374"
---
# <a name="tabledef-object-dao"></a>Объект TableDef (DAO)

**Область применения**: Access 2013, Office 2013

Объект **TableDef** представляет сохраненное определение основной или связанной таблицы (только для рабочих областей Microsoft Access).

## <a name="remarks"></a>Примечания

Работа с определением таблицы выполняется с помощью объекта **TableDef** и его методов и свойств. Например, вы можете:

- Проверить в базе данных структуру полей и индексов любой локальной, связанной или внешней таблицы.

- Указать или возвратить сведения о связанных таблицах с помощью свойств **Connect** и **SourceTableName**, а также обновить подключения к связанным таблицам с помощью метода **RefreshLink**.

- Установить или возвратить условия проверки с помощью свойств **ValidationRule** и **ValidationText**.

- Создать на основе определения таблицы объект **Recordset** табличного типа, динамического подмножества данных, динамического типа, моментального снимка или однонаправленного типа с помощью метода **OpenRecordset**.

Для основных таблиц свойство **RecordCount** содержит число записей в указанной таблице базы данных. Для связанных таблиц свойство **RecordCount** всегда имеет значение -1.

Чтобы создать новый объект **TableDef**, используйте метод **[CreateTableDef](database-createtabledef-method-dao.md)**.

### <a name="to-add-a-field-to-a-table"></a>Добавление поля в таблицу

1.  Убедитесь, что закрыты все объекты **[Recordset](recordset-object-dao.md)**, основанные на таблице.

2.  Используйте метод **CreateField**, чтобы создать переменную объекта **Field** и указать ее свойства.

3.  Добавьте объект **Field** в коллекцию **Fields** объекта **TableDef** с помощью метода **Append**.

Можно удалить объект **Field** из коллекции **TableDefs**, если ему не назначены никакие индексы, однако при этом будут потеряны данные этого поля.

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a>Создание в базе данных таблицы, готовой для новых записей

1.  Чтобы создать объект **TableDef**, используйте метод **CreateTableDef**.

2.  Настройте его свойства.

3.  Для каждого поля в таблице используйте метод **CreateField**, чтобы создать переменную объекта **Field** и указать ее свойства.

4.  Добавьте поля в коллекцию **Fields** объекта **TableDef** с помощью метода **Append**.

5.  Добавьте новый объект **TableDef** в коллекцию **TableDefs** объекта **Database** с помощью метода **Append**.

Связанная таблица подключается к базе данных с помощью свойств **SourceTableName** и **Connect** объекта **TableDef**.

### <a name="to-link-a-table-to-a-database"></a>Связывание таблицы с базой данных

1.  Чтобы создать объект **TableDef**, используйте метод **CreateTableDef**.

2.  Установите его свойства **Connect** и **SourceTableName** (и свойство **Attributes** при необходимости).

3.  Используйте метод **Append**, чтобы добавить его в коллекцию **TableDefs** объекта **Database**.

Чтобы сослаться на объект **TableDef** в коллекции по его порядковому номеру или по его свойству**Name**, используйте любую из указанных ниже синтаксических форм.

**TableDefs**(0)

**TableDefs**("name")

**TableDefs**\!\[имя\]

## <a name="example"></a>Пример

В этом примере создается новый объект **TableDef**, который добавляется в коллекцию **TableDefs** объекта базы данных Northwind. Затем перечисляются коллекции **TableDefs** и **Properties** нового объекта **TableDef**.

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

В этом примере создается новый объект **TableDef** в базе данных Northwind.

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

В приведенном ниже примере показано, как создать вычисляемое поле. Метод CreateField создает поле с именем **FullName**. Затем для свойства Expression устанавливается выражение, вычисляющее значение поля.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```
