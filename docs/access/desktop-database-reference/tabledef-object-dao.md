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
# <a name="tabledef-object-dao"></a><span data-ttu-id="82aee-102">TableDef Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="82aee-102">TableDef Object (DAO)</span></span>

<span data-ttu-id="82aee-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="82aee-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="82aee-104">Объект **TableDef** представляет сохраненные определение базовая таблица или связанной таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82aee-104">A **TableDef** object represents the stored definition of a base table or a linked table (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="82aee-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="82aee-105">Remarks</span></span>

<span data-ttu-id="82aee-106">Работа с помощью объекта **TableDef** и его методы и свойства определения таблицы.</span><span class="sxs-lookup"><span data-stu-id="82aee-106">You manipulate a table definition using a **TableDef** object and its methods and properties.</span></span> <span data-ttu-id="82aee-107">Например можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="82aee-107">For example, you can:</span></span>

- <span data-ttu-id="82aee-108">Анализ структуры поля и индекс любой локальной, связанные или внешним таблицы в базе данных.</span><span class="sxs-lookup"><span data-stu-id="82aee-108">Examine the field and index structure of any local, linked, or external table in a database.</span></span>

- <span data-ttu-id="82aee-109">Использование свойств **подключения** и **SourceTableName** задает или возвращает сведения о связанных таблиц, а метод **RefreshLink** для обновления подключений связанные таблицы.</span><span class="sxs-lookup"><span data-stu-id="82aee-109">Use the **Connect** and **SourceTableName** properties to set or return information about linked tables, and use the **RefreshLink** method to update connections to linked tables.</span></span>

- <span data-ttu-id="82aee-110">Использование свойств **значение** и **сообщение об ошибке** или возвращает условия проверки данных.</span><span class="sxs-lookup"><span data-stu-id="82aee-110">Use the **ValidationRule** and **ValidationText** properties to set or return validation conditions.</span></span>

- <span data-ttu-id="82aee-111">Используйте метод **OpenRecordset** для создания таблицы –, динамический набор –, динамической –, моментальный снимок – или объекта **набора записей** прямого — только — тип, на основе определения таблицы.</span><span class="sxs-lookup"><span data-stu-id="82aee-111">Use the **OpenRecordset** method to create a table–, dynaset–, dynamic–, snapshot–, or forward–only–type **Recordset** object, based on the table definition.</span></span>

<span data-ttu-id="82aee-112">Для базовых таблиц свойство **RecordCount** содержит число записей в таблице указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="82aee-112">For base tables, the **RecordCount** property contains the number of records in the specified database table.</span></span> <span data-ttu-id="82aee-113">Связанные таблицы значение свойства **RecordCount** всегда – 1.</span><span class="sxs-lookup"><span data-stu-id="82aee-113">For linked tables, the **RecordCount** property setting is always –1.</span></span>

<span data-ttu-id="82aee-114">Чтобы создать новый объект **TableDef** , используйте метод **[CreateTableDef](database-createtabledef-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="82aee-114">To create a new **TableDef** object, use the **[CreateTableDef](database-createtabledef-method-dao.md)** method.</span></span>

### <a name="to-add-a-field-to-a-table"></a><span data-ttu-id="82aee-115">Добавление поля в таблицу</span><span class="sxs-lookup"><span data-stu-id="82aee-115">To add a field to a table</span></span>

1.  <span data-ttu-id="82aee-116">Убедитесь в том, что любые объекты **[набора записей](recordset-object-dao.md)** на основе таблицы все закрыты.</span><span class="sxs-lookup"><span data-stu-id="82aee-116">Make sure any **[Recordset](recordset-object-dao.md)** objects based on the table are all closed.</span></span>

2.  <span data-ttu-id="82aee-117">Метод **CreateField** используется для создания переменной объекта **поля** и задайте его свойства.</span><span class="sxs-lookup"><span data-stu-id="82aee-117">Use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

3.  <span data-ttu-id="82aee-118">Метод **Append** используется для добавления объекта **поля** в коллекцию **полей** объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="82aee-118">Use the **Append** method to add the **Field** object to the **Fields** collection of the **TableDef** object.</span></span>

<span data-ttu-id="82aee-119">Можно удалить объект **поля** из коллекции **TableDefs** , если он не назначен индексы, но будут потеряны данных в поле.</span><span class="sxs-lookup"><span data-stu-id="82aee-119">You can delete a **Field** object from a **TableDefs** collection if it doesn't have any indexes assigned to it, but you will lose the field's data.</span></span>

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a><span data-ttu-id="82aee-120">Для создания таблицы, которая будет готов для добавления новых записей в базе данных</span><span class="sxs-lookup"><span data-stu-id="82aee-120">To create a table that is ready for new records in a database</span></span>

1.  <span data-ttu-id="82aee-121">Используйте метод **CreateTableDef** для создания объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="82aee-121">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="82aee-122">Задайте его свойства.</span><span class="sxs-lookup"><span data-stu-id="82aee-122">Set its properties.</span></span>

3.  <span data-ttu-id="82aee-123">Для каждого поля в таблице используйте метод **CreateField** для создания переменной объекта **поля** и задайте его свойства.</span><span class="sxs-lookup"><span data-stu-id="82aee-123">For each field in the table, use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

4.  <span data-ttu-id="82aee-124">Метод **Append** используется для добавления поля в коллекцию **полей** объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="82aee-124">Use the **Append** method to add the fields to the **Fields** collection of the **TableDef** object.</span></span>

5.  <span data-ttu-id="82aee-125">Метод **Append** используется для добавления нового объекта **TableDef** в коллекцию **TableDefs** объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="82aee-125">Use the **Append** method to add the new **TableDef** object to the **TableDefs** collection of the **Database** object.</span></span>

<span data-ttu-id="82aee-126">По **SourceTableName** и **Подключить** свойства объекта **TableDef** связанной таблицы подключение к базе данных.</span><span class="sxs-lookup"><span data-stu-id="82aee-126">A linked table is connected to the database by the **SourceTableName** and **Connect** properties of the **TableDef** object.</span></span>

### <a name="to-link-a-table-to-a-database"></a><span data-ttu-id="82aee-127">Чтобы связать таблицы с базой данных</span><span class="sxs-lookup"><span data-stu-id="82aee-127">To link a table to a database</span></span>

1.  <span data-ttu-id="82aee-128">Используйте метод **CreateTableDef** для создания объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="82aee-128">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="82aee-129">Задайте его свойства **подключения** и **SourceTableName** (и, при необходимости, его свойство **атрибуты** ).</span><span class="sxs-lookup"><span data-stu-id="82aee-129">Set its **Connect** and **SourceTableName** properties (and optionally, its **Attributes** property).</span></span>

3.  <span data-ttu-id="82aee-130">Метод **Append** используется для добавления его в коллекцию **TableDefs** **базы данных**.</span><span class="sxs-lookup"><span data-stu-id="82aee-130">Use the **Append** method to add it to the **TableDefs** collection of a **Database**.</span></span>

<span data-ttu-id="82aee-131">Для ссылки на объект **TableDef** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="82aee-131">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="82aee-132">**TableDefs** (0)</span><span class="sxs-lookup"><span data-stu-id="82aee-132">**TableDefs**(0)</span></span>

<span data-ttu-id="82aee-133">**TableDefs** («имя»)</span><span class="sxs-lookup"><span data-stu-id="82aee-133">**TableDefs**("name")</span></span>

<span data-ttu-id="82aee-134">**TableDefs**\!\[имя\]</span><span class="sxs-lookup"><span data-stu-id="82aee-134">**TableDefs**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="82aee-135">Пример</span><span class="sxs-lookup"><span data-stu-id="82aee-135">Example</span></span>

<span data-ttu-id="82aee-136">В этом примере создается новый объект **TableDef** и добавляет его в коллекцию **TableDefs** объекта базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="82aee-136">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object.</span></span> <span data-ttu-id="82aee-137">Затем выполняется перечисление коллекции **TableDefs** и коллекции **свойств** нового **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="82aee-137">It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

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

<span data-ttu-id="82aee-138">В этом примере создается новый объект **TableDef** базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="82aee-138">This example creates a new **TableDef** object in the Northwind database.</span></span>

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

<span data-ttu-id="82aee-139">Следующий пример демонстрирует создание вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="82aee-139">The following example shows how to create a calculated field.</span></span> <span data-ttu-id="82aee-140">Метод CreateField создает поле с именем **полное имя**.</span><span class="sxs-lookup"><span data-stu-id="82aee-140">The CreateField method creates a field named **FullName**.</span></span> <span data-ttu-id="82aee-141">Выражение затем задано значение выражения, вычисляющий значение поля.</span><span class="sxs-lookup"><span data-stu-id="82aee-141">The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="82aee-142">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="82aee-142">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
