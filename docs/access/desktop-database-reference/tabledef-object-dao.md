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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726346"
---
# <a name="tabledef-object-dao"></a><span data-ttu-id="bda14-102">Объект TableDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="bda14-102">TableDef Object (DAO)</span></span>

<span data-ttu-id="bda14-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bda14-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bda14-104">Объект **TableDef** представляет сохраненное определение основной или связанной таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bda14-104">A **TableDef** object represents the stored definition of a base table or a linked table (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="bda14-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="bda14-105">Remarks</span></span>

<span data-ttu-id="bda14-106">Работа с определением таблицы выполняется с помощью объекта **TableDef** и его методов и свойств.</span><span class="sxs-lookup"><span data-stu-id="bda14-106">You manipulate a table definition using a **TableDef** object and its methods and properties.</span></span> <span data-ttu-id="bda14-107">Например, вы можете:</span><span class="sxs-lookup"><span data-stu-id="bda14-107">For example, you can use:</span></span>

- <span data-ttu-id="bda14-108">Проверить в базе данных структуру полей и индексов любой локальной, связанной или внешней таблицы.</span><span class="sxs-lookup"><span data-stu-id="bda14-108">Examine the field and index structure of any local, linked, or external table in a database.</span></span>

- <span data-ttu-id="bda14-109">Указать или возвратить сведения о связанных таблицах с помощью свойств **Connect** и **SourceTableName**, а также обновить подключения к связанным таблицам с помощью метода **RefreshLink**.</span><span class="sxs-lookup"><span data-stu-id="bda14-109">Use the **Connect** and **SourceTableName** properties to set or return information about linked tables, and use the **RefreshLink** method to update connections to linked tables.</span></span>

- <span data-ttu-id="bda14-110">Установить или возвратить условия проверки с помощью свойств **ValidationRule** и **ValidationText**.</span><span class="sxs-lookup"><span data-stu-id="bda14-110">Use the **ValidationRule** and **ValidationText** properties to set or return validation conditions.</span></span>

- <span data-ttu-id="bda14-111">Создать на основе определения таблицы объект **Recordset** табличного типа, динамического подмножества данных, динамического типа, моментального снимка или однонаправленного типа с помощью метода **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="bda14-111">Use the **OpenRecordset** method to create a table–, dynaset–, dynamic–, snapshot–, or forward–only–type **Recordset** object, based on the table definition.</span></span>

<span data-ttu-id="bda14-112">Для основных таблиц свойство **RecordCount** содержит число записей в указанной таблице базы данных.</span><span class="sxs-lookup"><span data-stu-id="bda14-112">For base tables, the **RecordCount** property contains the number of records in the specified database table.</span></span> <span data-ttu-id="bda14-113">Для связанных таблиц свойство **RecordCount** всегда имеет значение -1.</span><span class="sxs-lookup"><span data-stu-id="bda14-113">For linked tables, the **RecordCount** property setting is always –1.</span></span>

<span data-ttu-id="bda14-114">Чтобы создать новый объект **TableDef**, используйте метод **[CreateTableDef](database-createtabledef-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="bda14-114">To create a new **TableDef** object, use the **[CreateTableDef](database-createtabledef-method-dao.md)** method.</span></span>

### <a name="to-add-a-field-to-a-table"></a><span data-ttu-id="bda14-115">Добавление поля в таблицу</span><span class="sxs-lookup"><span data-stu-id="bda14-115">To add a field to a table</span></span>

1.  <span data-ttu-id="bda14-116">Убедитесь, что закрыты все объекты **[Recordset](recordset-object-dao.md)**, основанные на таблице.</span><span class="sxs-lookup"><span data-stu-id="bda14-116">Make sure any **[Recordset](recordset-object-dao.md)** objects based on the table are all closed.</span></span>

2.  <span data-ttu-id="bda14-117">Используйте метод **CreateField**, чтобы создать переменную объекта **Field** и указать ее свойства.</span><span class="sxs-lookup"><span data-stu-id="bda14-117">Use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

3.  <span data-ttu-id="bda14-118">Добавьте объект **Field** в коллекцию **Fields** объекта **TableDef** с помощью метода **Append**.</span><span class="sxs-lookup"><span data-stu-id="bda14-118">Use the **Append** method to add the **Field** object to the **Fields** collection of the **TableDef** object.</span></span>

<span data-ttu-id="bda14-119">Можно удалить объект **Field** из коллекции **TableDefs**, если ему не назначены никакие индексы, однако при этом будут потеряны данные этого поля.</span><span class="sxs-lookup"><span data-stu-id="bda14-119">You can delete a **Field** object from a **TableDefs** collection if it doesn't have any indexes assigned to it, but you will lose the field's data.</span></span>

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a><span data-ttu-id="bda14-120">Создание в базе данных таблицы, готовой для новых записей</span><span class="sxs-lookup"><span data-stu-id="bda14-120">To create a table that is ready for new records in a database</span></span>

1.  <span data-ttu-id="bda14-121">Чтобы создать объект **TableDef**, используйте метод **CreateTableDef**.</span><span class="sxs-lookup"><span data-stu-id="bda14-121">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="bda14-122">Настройте его свойства.</span><span class="sxs-lookup"><span data-stu-id="bda14-122">Set its properties.</span></span>

3.  <span data-ttu-id="bda14-123">Для каждого поля в таблице используйте метод **CreateField**, чтобы создать переменную объекта **Field** и указать ее свойства.</span><span class="sxs-lookup"><span data-stu-id="bda14-123">For each field in the table, use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

4.  <span data-ttu-id="bda14-124">Добавьте поля в коллекцию **Fields** объекта **TableDef** с помощью метода **Append**.</span><span class="sxs-lookup"><span data-stu-id="bda14-124">Use the **Append** method to add the fields to the **Fields** collection of the **TableDef** object.</span></span>

5.  <span data-ttu-id="bda14-125">Добавьте новый объект **TableDef** в коллекцию **TableDefs** объекта **Database** с помощью метода **Append**.</span><span class="sxs-lookup"><span data-stu-id="bda14-125">Use the **Append** method to add the new **TableDef** object to the **TableDefs** collection of the **Database** object.</span></span>

<span data-ttu-id="bda14-126">Связанная таблица подключается к базе данных с помощью свойств **SourceTableName** и **Connect** объекта **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="bda14-126">A linked table is connected to the database by the **SourceTableName** and **Connect** properties of the **TableDef** object.</span></span>

### <a name="to-link-a-table-to-a-database"></a><span data-ttu-id="bda14-127">Связывание таблицы с базой данных</span><span class="sxs-lookup"><span data-stu-id="bda14-127">To link a table to a database</span></span>

1.  <span data-ttu-id="bda14-128">Чтобы создать объект **TableDef**, используйте метод **CreateTableDef**.</span><span class="sxs-lookup"><span data-stu-id="bda14-128">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="bda14-129">Установите его свойства **Connect** и **SourceTableName** (и свойство **Attributes** при необходимости).</span><span class="sxs-lookup"><span data-stu-id="bda14-129">Set its **Connect** and **SourceTableName** properties (and optionally, its **Attributes** property).</span></span>

3.  <span data-ttu-id="bda14-130">Используйте метод **Append**, чтобы добавить его в коллекцию **TableDefs** объекта **Database**.</span><span class="sxs-lookup"><span data-stu-id="bda14-130">Use the **Append** method to add it to the **TableDefs** collection of a **Database**.</span></span>

<span data-ttu-id="bda14-131">Чтобы сослаться на объект **TableDef** в коллекции по его порядковому номеру или по его свойству**Name**, используйте любую из указанных ниже синтаксических форм.</span><span class="sxs-lookup"><span data-stu-id="bda14-131">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="bda14-132">**TableDefs**(0)</span><span class="sxs-lookup"><span data-stu-id="bda14-132">**TableDefs**(0)</span></span>

<span data-ttu-id="bda14-133">**TableDefs**("имя")</span><span class="sxs-lookup"><span data-stu-id="bda14-133">**TableDefs**("name")</span></span>

<span data-ttu-id="bda14-134">**TableDefs**\!\[имя\]</span><span class="sxs-lookup"><span data-stu-id="bda14-134">**TableDefs**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="bda14-135">Пример</span><span class="sxs-lookup"><span data-stu-id="bda14-135">Example</span></span>

<span data-ttu-id="bda14-136">В этом примере создается новый объект **TableDef**, который добавляется в коллекцию **TableDefs** объекта базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="bda14-136">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object.</span></span> <span data-ttu-id="bda14-137">Затем перечисляются коллекции **TableDefs** и **Properties** нового объекта **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="bda14-137">It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

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

<span data-ttu-id="bda14-138">В этом примере создается новый объект **TableDef** в базе данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="bda14-138">This example creates a new **TableDef** object in the Northwind database.</span></span>

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

<span data-ttu-id="bda14-139">В приведенном ниже примере показано, как создать вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="bda14-139">The following example shows how to create a custom field for a list.</span></span> <span data-ttu-id="bda14-140">Метод CreateField создает поле с именем **FullName**.</span><span class="sxs-lookup"><span data-stu-id="bda14-140">The CreateField method creates a field named **FullName**.</span></span> <span data-ttu-id="bda14-141">Затем для свойства Expression устанавливается выражение, вычисляющее значение поля.</span><span class="sxs-lookup"><span data-stu-id="bda14-141">The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="bda14-142">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="bda14-142">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
