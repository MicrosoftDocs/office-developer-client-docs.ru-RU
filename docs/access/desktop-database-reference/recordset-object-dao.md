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
# <a name="recordset-object-dao"></a><span data-ttu-id="224fb-102">Recordset Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="224fb-102">Recordset Object (DAO)</span></span>

<span data-ttu-id="224fb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="224fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="224fb-104">Объект **набора записей** представляет записей в базовой таблице или записей, в результате выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="224fb-104">A **Recordset** object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="remarks"></a><span data-ttu-id="224fb-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="224fb-105">Remarks</span></span>

<span data-ttu-id="224fb-106">Для работы с данными в базе данных на уровне записей используйте объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="224fb-106">You use **Recordset** objects to manipulate data in a database at the record level.</span></span> <span data-ttu-id="224fb-107">При использовании объектов DAO работы с данным почти полностью с помощью объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="224fb-107">When you use DAO objects, you manipulate data almost entirely using **Recordset** objects.</span></span> <span data-ttu-id="224fb-108">Все объекты **наборов записей** , созданные с помощью записей (строк) и полей (столбцов).</span><span class="sxs-lookup"><span data-stu-id="224fb-108">All **Recordset** objects are constructed using records (rows) and fields (columns).</span></span> <span data-ttu-id="224fb-109">Существует пять типов объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="224fb-109">There are five types of **Recordset** objects:</span></span>

- <span data-ttu-id="224fb-110">Тип таблицы записей — представление в коде базовой таблицы, которые можно использовать для добавления, изменения или удаления записей из одной таблицы базы данных (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="224fb-110">Table-type Recordset— representation in code of a base table that you can use to add, change, or delete records from a single database table (Microsoft Access workspaces only).</span></span>

- <span data-ttu-id="224fb-111">Копирование или изменение — результат запроса, который может иметь обновляемых записей.</span><span class="sxs-lookup"><span data-stu-id="224fb-111">Dynaset-type Recordset— the result of a query that can have updatable records.</span></span> <span data-ttu-id="224fb-112">Объект **набора записей** добавляющий представляют собой динамический набор записей, которые можно использовать для добавления, изменения или удаления записей из базовой таблицы базы данных или таблицы.</span><span class="sxs-lookup"><span data-stu-id="224fb-112">A dynaset-type **Recordset** object is a dynamic set of records that you can use to add, change, or delete records from an underlying database table or tables.</span></span> <span data-ttu-id="224fb-113">Объект типа динамического **набора записей** может содержать поля из одного или нескольких таблиц в базе данных.</span><span class="sxs-lookup"><span data-stu-id="224fb-113">A dynaset-type **Recordset** object can contain fields from one or more tables in a database.</span></span> <span data-ttu-id="224fb-114">Этот тип соответствует курсор набора ключей ODBC.</span><span class="sxs-lookup"><span data-stu-id="224fb-114">This type corresponds to an ODBC keyset cursor.</span></span>

- <span data-ttu-id="224fb-115">Моментальный снимок типа записей — статические копию набора записей, которые можно использовать для поиска данных и создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="224fb-115">Snapshot-type Recordset— a static copy of a set of records that you can use to find data or generate reports.</span></span> <span data-ttu-id="224fb-116">Объект типа **набора записей** может содержать поля из одного или нескольких таблиц в базе данных, но не могут быть обновлены.</span><span class="sxs-lookup"><span data-stu-id="224fb-116">A snapshot-type **Recordset** object can contain fields from one or more tables in a database but can't be updated.</span></span> <span data-ttu-id="224fb-117">Этот тип соответствует статическим курсором ODBC.</span><span class="sxs-lookup"><span data-stu-id="224fb-117">This type corresponds to an ODBC static cursor.</span></span>

- <span data-ttu-id="224fb-118">Прямого только для типа записей — аналогична моментальный снимок, за исключением того, что предоставляется не курсора.</span><span class="sxs-lookup"><span data-stu-id="224fb-118">Forward-only-type Recordset— identical to a snapshot except that no cursor is provided.</span></span> <span data-ttu-id="224fb-119">Можно выполнять только прокрутку вперед записей.</span><span class="sxs-lookup"><span data-stu-id="224fb-119">You can only scroll forward through records.</span></span> <span data-ttu-id="224fb-120">Это повышает производительность в ситуациях, только чтобы сделать один проход в наборе результатов.</span><span class="sxs-lookup"><span data-stu-id="224fb-120">This improves performance in situations where you only need to make a single pass through a result set.</span></span> <span data-ttu-id="224fb-121">Этот тип соответствует только вперед текущей позиции ODBC.</span><span class="sxs-lookup"><span data-stu-id="224fb-121">This type corresponds to an ODBC forward-only cursor.</span></span>

- <span data-ttu-id="224fb-122">Записей динамического типа — результатов запроса изменять из одного или нескольких базовые таблицы, в которых можно добавить, изменения или удаления записей из возвращающие строки запроса.</span><span class="sxs-lookup"><span data-stu-id="224fb-122">Dynamic-type Recordset— a query result set from one or more base tables in which you can add, change, or delete records from a row-returning query.</span></span> <span data-ttu-id="224fb-123">Более того другим пользователям добавление, удаление или изменение в базовые таблицы также отображаются записи в наборе **записей**.</span><span class="sxs-lookup"><span data-stu-id="224fb-123">Further, records other users add, delete, or edit in the base tables also appear in your **Recordset**.</span></span> <span data-ttu-id="224fb-124">Этот тип соответствует динамического курсора ODBC (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="224fb-124">This type corresponds to an ODBC dynamic cursor (ODBCDirect workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="224fb-125">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="224fb-125">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="224fb-126">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="224fb-126">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="224fb-127">Можно выбрать тип объекта **набора записей** , которые необходимо создать с помощью метода **OpenRecordset** аргумент типа.</span><span class="sxs-lookup"><span data-stu-id="224fb-127">You can choose the type of **Recordset** object you want to create using the type argument of the **OpenRecordset** method.</span></span>

<span data-ttu-id="224fb-128">В рабочей области Microsoft Access Если не указать тип DAO предпринимается попытка создать тип **набора записей** с большинство функциональных возможностей, начиная с таблицей.</span><span class="sxs-lookup"><span data-stu-id="224fb-128">In a Microsoft Access workspace, if you don't specify a type, DAO attempts to create the type of **Recordset** with the most functionality available, starting with table.</span></span> <span data-ttu-id="224fb-129">Если этот тип не поддерживается, DAO пытается подмножества, а затем моментальный снимок и, наконец, однонаправленные тип объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="224fb-129">If this type isn't available, DAO attempts a dynaset, then a snapshot, and finally a forward-only type **Recordset** object.</span></span>

<span data-ttu-id="224fb-130">В рабочей области технология ODBCDirect Если не указать тип DAO пытается создать тип **набора записей** с быстрый ответ на запрос, начиная с последовательного доступа.</span><span class="sxs-lookup"><span data-stu-id="224fb-130">In an ODBCDirect workspace, if you don't specify a type, DAO attempts to create the type of **Recordset** with the fastest query response, starting with forward-only.</span></span> <span data-ttu-id="224fb-131">Если этот тип не поддерживается, DAO пытается моментальный снимок, а затем подмножества и, наконец, объект **набора записей** динамического типа.</span><span class="sxs-lookup"><span data-stu-id="224fb-131">If this type isn't available, DAO attempts a snapshot, then a dynaset, and finally a dynamic- type **Recordset** object.</span></span>

<span data-ttu-id="224fb-132">При создании объекта **набора записей** с помощью объекта **[TableDef](tabledef-object-dao.md)** несвязанных в рабочей области Microsoft Access, создаются в таблице объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="224fb-132">When creating a **Recordset** object using a non-linked **[TableDef](tabledef-object-dao.md)** object in a Microsoft Access workspace, table-type **Recordset** objects are created.</span></span> <span data-ttu-id="224fb-133">С помощью связанных таблиц и таблиц в базах данных ODBC engine подключенной базы данных Microsoft Access можно создавать только динамического или объектов **наборов записей** типа снимка.</span><span class="sxs-lookup"><span data-stu-id="224fb-133">Only dynaset-type or snapshot-type **Recordset** objects can be created with linked tables or tables in Microsoft Access database engine-connected ODBC databases.</span></span>

<span data-ttu-id="224fb-134">Новый объект **набора записей** автоматически добавляется в коллекцию **наборов записей** при открытии объекта и автоматически удаляются при закрытии.</span><span class="sxs-lookup"><span data-stu-id="224fb-134">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the object, and is automatically removed when you close it.</span></span>

> [!NOTE]
> <span data-ttu-id="224fb-135">Если использовать переменные для представления объекта **набора записей** и объекта **базы данных** , содержащее **набор записей**, убедитесь, что переменные иметь те же области или время жизни.</span><span class="sxs-lookup"><span data-stu-id="224fb-135">If you use variables to represent a **Recordset** object and the **Database** object that contains the **Recordset**, make sure the variables have the same scope, or lifetime.</span></span> <span data-ttu-id="224fb-136">Например если объявить открытую переменную, которая представляет собой объект- **записей** , убедитесь, что переменной, которая представляет базе **базы данных** , содержащий **записей** также общедоступный или объявляется в **Sub** или **Function** процедуры, с помощью ключевое слово **Static** .</span><span class="sxs-lookup"><span data-stu-id="224fb-136">For example, if you declare a public variable that represents a **Recordset** object, make sure the variable that represents the **Database** containing the **Recordset** is also public, or is declared in a **Sub** or **Function** procedure using the **Static** keyword.</span></span>

<span data-ttu-id="224fb-137">Можно создать любое количество переменных объекта **набора записей** при необходимости.</span><span class="sxs-lookup"><span data-stu-id="224fb-137">You can create as many **Recordset** object variables as needed.</span></span> <span data-ttu-id="224fb-138">Объекты различных **наборов записей** можно получить доступ к таблиц, запросов и полей без конфликтов.</span><span class="sxs-lookup"><span data-stu-id="224fb-138">Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="224fb-139">Динамический набор – моментальный снимок – и прямого — только — тип объектов **наборов записей** хранятся в локальной памяти.</span><span class="sxs-lookup"><span data-stu-id="224fb-139">Dynaset–, snapshot–, and forward–only–type **Recordset** objects are stored in local memory.</span></span> <span data-ttu-id="224fb-140">Если в локальной памяти для хранения данных, не хватает места, ядро базы данных Microsoft Access сохраняет дополнительные данные во ВРЕМЕННЫЙ дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="224fb-140">If there isn't enough space in local memory to store the data, the Microsoft Access database engine saves the additional data to TEMP disk space.</span></span> <span data-ttu-id="224fb-141">Если исчерпано этого пространства, то перехватываемые возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="224fb-141">If this space is exhausted, a trappable error occurs.</span></span>

<span data-ttu-id="224fb-142">По умолчанию коллекции объекта **набора записей** представляет коллекцию **полей** , а свойство **[Value](field-value-property-dao.md)** является свойством по умолчанию объекта **[поля](field-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="224fb-142">The default collection of a **Recordset** object is the **Fields** collection, and the default property of a **[Field](field-object-dao.md)** object is the **[Value](field-value-property-dao.md)** property.</span></span> <span data-ttu-id="224fb-143">Используйте эти значения по умолчанию для упрощения кода.</span><span class="sxs-lookup"><span data-stu-id="224fb-143">Use these defaults to simplify your code.</span></span>

<span data-ttu-id="224fb-144">При создании объекта **набора записей** текущей записи располагается первой записи при наличии записей.</span><span class="sxs-lookup"><span data-stu-id="224fb-144">When you create a **Recordset** object, the current record is positioned to the first record if there are any records.</span></span> <span data-ttu-id="224fb-145">Если нет записей, **RecordCount** свойство имеет значение 0, а также \*\* **BOF** или **EOF** параметров выполняются\*\*.</span><span class="sxs-lookup"><span data-stu-id="224fb-145">If there are no records, the **RecordCount** property setting is 0, and the **BOF** and **EOF** property settings are **True**.</span></span>

<span data-ttu-id="224fb-146">**MoveNext**, **MovePrevious**, **MoveFirst**и **MoveLast** методы можно использовать для изменения положения текущей записи.</span><span class="sxs-lookup"><span data-stu-id="224fb-146">You can use the **MoveNext**, **MovePrevious**, **MoveFirst**, and **MoveLast** methods to reposition the current record.</span></span> <span data-ttu-id="224fb-147">Объекты **набора записей** прямого — только — тип поддерживает только метод **MoveNext** .</span><span class="sxs-lookup"><span data-stu-id="224fb-147">Forward–only–type **Recordset** objects support only the **MoveNext** method.</span></span> <span data-ttu-id="224fb-148">При использовании методов перемещения посетите каждая запись (или «рассмотрение» **набора записей**), можно использовать свойства **BOF** и **EOF** на наличие начала или окончания объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="224fb-148">When using the Move methods to visit each record (or "walk" through the **Recordset**), you can use the **BOF** and **EOF** properties to check for the beginning or end of the **Recordset** object.</span></span>

<span data-ttu-id="224fb-149">С и моментальный снимок добавляющий объектов **наборов записей** в рабочую область для Microsoft Access, можно также использовать методы поиска, такие как **FindFirst**поиск определенной записи на основе критериев.</span><span class="sxs-lookup"><span data-stu-id="224fb-149">With dynaset- and snapshot-type **Recordset** objects in a Microsoft Access workspace, you can also use the Find methods, such as **FindFirst**, to locate a specific record based on criteria.</span></span> <span data-ttu-id="224fb-150">Если запись не найден, свойство **NoMatch** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="224fb-150">If the record isn't found, the **NoMatch** property is set to **True**.</span></span> <span data-ttu-id="224fb-151">Объектам-таблица тип **набора записей** для проверки записей с помощью метода **Seek** .</span><span class="sxs-lookup"><span data-stu-id="224fb-151">For table-type **Recordset** objects, you can scan records using the **Seek** method.</span></span>

<span data-ttu-id="224fb-152">Свойство **Type** указывает тип объекта **Recordset** , созданного и свойство **с возможностью записи** указывает, можно ли изменить записи объекта.</span><span class="sxs-lookup"><span data-stu-id="224fb-152">The **Type** property indicates the type of **Recordset** object created, and the **Updatable** property indicates whether you can change the object's records.</span></span>

<span data-ttu-id="224fb-153">Сведения о структуре базовая таблица, таких как имена и типы данных каждого объекта **поля** и любые объекты **индекса** хранится в объекте **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="224fb-153">Information about the structure of a base table, such as the names and data types of each **Field** object and any **Index** objects, is stored in a **TableDef** object.</span></span>

<span data-ttu-id="224fb-154">Для ссылки на объект **набора записей** в коллекции по его порядковый номер или по **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="224fb-154">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="224fb-155">**Наборы записей** (0)</span><span class="sxs-lookup"><span data-stu-id="224fb-155">**Recordsets**(0)</span></span>

- <span data-ttu-id="224fb-156">**Наборы записей** («имя»)</span><span class="sxs-lookup"><span data-stu-id="224fb-156">**Recordsets**("name")</span></span>

- <span data-ttu-id="224fb-157">**Наборы записей**\!\[имя\]</span><span class="sxs-lookup"><span data-stu-id="224fb-157">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="224fb-158">Объект **набора записей** можно открыть из одного источника данных или базы данных более одного раза, Создание повторяющихся имен в коллекции **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="224fb-158">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection.</span></span> <span data-ttu-id="224fb-159">Следует назначить объектов **наборов записей** объектных переменных и обращаться к ним с именем переменной.</span><span class="sxs-lookup"><span data-stu-id="224fb-159">You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="224fb-160">Пример</span><span class="sxs-lookup"><span data-stu-id="224fb-160">Example</span></span>

<span data-ttu-id="224fb-161">В этом примере демонстрируется **набора записей** объекты и коллекции **наборов записей** , открыв четыре различных типов **наборов записей**, перечисления коллекции наборов записей текущей **базы данных**и перечисление \*\* Свойства\*\* коллекцию каждого **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="224fb-161">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

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

В этом примере используется метод **OpenRecordset** Открытие пять разных объектов **набора записей** и отображения их содержимого. <span data-ttu-id="224fb-163">Процедура OpenRecordsetOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="224fb-163">The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="224fb-164">В этом примере открывает объект **набора записей** динамического типа и перечисление ее записи.</span><span class="sxs-lookup"><span data-stu-id="224fb-164">This example opens a dynamic-type **Recordset** object and enumerates its records.</span></span>

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

<span data-ttu-id="224fb-165">В этом примере открывается типа динамического **набора записей** и показывает область, к которому его поля, обновляемых.</span><span class="sxs-lookup"><span data-stu-id="224fb-165">This example opens a dynaset-type **Recordset** and shows the extent to which its fields are updatable.</span></span>

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

<span data-ttu-id="224fb-166">В этом примере открывается прямого только для типа **записей**, показывает, характеристики его только для чтения и шаги по **набора записей** с помощью метода **MoveNext** .</span><span class="sxs-lookup"><span data-stu-id="224fb-166">This example opens a forward-only-type **Recordset**, demonstrates its read-only characteristics, and steps through the **Recordset** with the **MoveNext** method.</span></span>

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

<span data-ttu-id="224fb-167">В этом примере открывается типа **записей** и демонстрируются характеристики его только для чтения.</span><span class="sxs-lookup"><span data-stu-id="224fb-167">This example opens a snapshot-type **Recordset** and demonstrates its read-only characteristics.</span></span>

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

<span data-ttu-id="224fb-168">В этом примере открывается таблица тип **набора записей**, задает его свойства **Index** и перечисляет его записей.</span><span class="sxs-lookup"><span data-stu-id="224fb-168">This example opens a table-type **Recordset**, sets its **Index** property, and enumerates its records.</span></span>

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

<span data-ttu-id="224fb-169">Следующем примере показано, как использовать метод поиска для поиска записей в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="224fb-169">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="224fb-170">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="224fb-170">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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

<span data-ttu-id="224fb-171">Следующем примере показано, как открыть записей, основанный на параметр запроса.</span><span class="sxs-lookup"><span data-stu-id="224fb-171">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

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

<span data-ttu-id="224fb-172">Следующем примере показано, как открыть набор записей на основе таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="224fb-172">The following example shows how to open a Recordset based on a table or a query.</span></span>

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

<span data-ttu-id="224fb-173">Следующем примере показано, как открыть записей, на основе инструкции структурированный язык запросов (SQL).</span><span class="sxs-lookup"><span data-stu-id="224fb-173">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

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

<span data-ttu-id="224fb-174">Следующем примере показано, как использовать методы FindFirst и FindNext для поиска записей в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="224fb-174">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

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

<span data-ttu-id="224fb-175">Следующем примере показано, как скопировать результаты запроса на лист в новой книги Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="224fb-175">The following example shows how to copy the results of a query to a worksheet in a new Microsoft Excel workbook.</span></span>

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

