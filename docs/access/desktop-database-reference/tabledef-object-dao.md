---
title: TableDef Object (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef0a7c167321a45249fb022e0987a5f8d6364ea0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479806"
---
# <a name="tabledef-object-dao"></a>TableDef Object (DAO)

**Применимо к**: Access 2013 | Office 2013

Объект **TableDef** представляет сохраненные определение базовая таблица или связанной таблицы (только для рабочих областей Microsoft Access).

## <a name="remarks"></a>Замечания

Работа с помощью объекта **TableDef** и его методы и свойства определения таблицы. Например можно выполнить следующие действия.

- Анализ структуры поля и индекс любой локальной, связанные или внешним таблицы в базе данных.

- Использование свойств **подключения** и **SourceTableName** задает или возвращает сведения о связанных таблиц, а метод **RefreshLink** для обновления подключений связанные таблицы.

- Использование свойств **значение** и **сообщение об ошибке** или возвращает условия проверки данных.

- Используйте метод **OpenRecordset** для создания таблицы –, динамический набор –, динамической –, моментальный снимок – или объекта **набора записей** прямого — только — тип, на основе определения таблицы.

Для базовых таблиц свойство **RecordCount** содержит число записей в таблице указанной базы данных. Связанные таблицы значение свойства **RecordCount** всегда – 1.

Чтобы создать новый объект **TableDef** , используйте метод **[CreateTableDef](database-createtabledef-method-dao.md)** .

### <a name="to-add-a-field-to-a-table"></a>Добавление поля в таблицу

1.  Убедитесь в том, что любые объекты **[набора записей](recordset-object-dao.md)** на основе таблицы все закрыты.

2.  Метод **CreateField** используется для создания переменной объекта **поля** и задайте его свойства.

3.  Метод **Append** используется для добавления объекта **поля** в коллекцию **полей** объекта **TableDef** .

Можно удалить объект **поля** из коллекции **TableDefs** , если он не назначен индексы, но будут потеряны данных в поле.

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a>Для создания таблицы, которая будет готов для добавления новых записей в базе данных

1.  Используйте метод **CreateTableDef** для создания объекта **TableDef** .

2.  Задайте его свойства.

3.  Для каждого поля в таблице используйте метод **CreateField** для создания переменной объекта **поля** и задайте его свойства.

4.  Метод **Append** используется для добавления поля в коллекцию **полей** объекта **TableDef** .

5.  Метод **Append** используется для добавления нового объекта **TableDef** в коллекцию **TableDefs** объекта **базы данных** .

По **SourceTableName** и **Подключить** свойства объекта **TableDef** связанной таблицы подключение к базе данных.

### <a name="to-link-a-table-to-a-database"></a>Чтобы связать таблицы с базой данных

1.  Используйте метод **CreateTableDef** для создания объекта **TableDef** .

2.  Задайте его свойства **подключения** и **SourceTableName** (и, при необходимости, его свойство **атрибуты** ).

3.  Метод **Append** используется для добавления его в коллекцию **TableDefs** **базы данных**.

Для ссылки на объект **TableDef** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:

**TableDefs** (0)

**TableDefs** («имя»)

**TableDefs**\!\[имя\]

## <a name="example"></a>Пример

В этом примере создается новый объект **TableDef** и добавляет его в коллекцию **TableDefs** объекта базы данных Northwind. Затем выполняется перечисление коллекции **TableDefs** и коллекции **свойств** нового **TableDef**.

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

В этом примере создается новый объект **TableDef** базы данных Northwind.

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

Следующий пример демонстрирует создание вычисляемого поля. Метод CreateField создает поле с именем **полное имя**. Выражение затем задано значение выражения, вычисляющий значение поля.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
