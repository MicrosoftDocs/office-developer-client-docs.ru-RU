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
# <a name="recordset-object-dao"></a><span data-ttu-id="3324f-102">Объект Recordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="3324f-102">Recordset object (DAO)</span></span>

<span data-ttu-id="3324f-103">**Применяется для:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3324f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3324f-104">Объект **Recordset** представляет записи в базовой таблице или записи, получаемые в результате выполнения запросов.</span><span class="sxs-lookup"><span data-stu-id="3324f-104">A **Recordset** object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="remarks"></a><span data-ttu-id="3324f-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3324f-105">Remarks</span></span>

<span data-ttu-id="3324f-106">Вы можете использовать **Recordset**, чтобы управлять данными в базе данных на уровне записей.</span><span class="sxs-lookup"><span data-stu-id="3324f-106">You use **Recordset** objects to manipulate data in a database at the record level.</span></span> <span data-ttu-id="3324f-107">Если вы используете интерфейс DAO, вы можете управлять данными практически полностью с помощью объектов **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3324f-107">When you use DAO objects, you manipulate data almost entirely using **Recordset** objects.</span></span> <span data-ttu-id="3324f-108">Все объекты **Recordset** построены с использованием записей (строки) и полей (столбцы).</span><span class="sxs-lookup"><span data-stu-id="3324f-108">All **Recordset** objects are constructed using records (rows) and fields (columns).</span></span> <span data-ttu-id="3324f-109">Существует пять типов объектов **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="3324f-109">There are five types of **Recordset** objects:</span></span>

- <span data-ttu-id="3324f-110">Объект Recordset табличного типа — представление в коде базовой таблицы, которое вы можете использовать для добавления, изменения и удаления записей из таблицы одной базы данных (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3324f-110">Table-type Recordset— representation in code of a base table that you can use to add, change, or delete records from a single database table (Microsoft Access workspaces only).</span></span>

- <span data-ttu-id="3324f-111">Объект Recordset типа Dynaset — результат запроса, который может обновлять записи.</span><span class="sxs-lookup"><span data-stu-id="3324f-111">Dynaset-type Recordset— the result of a query that can have updatable records.</span></span> <span data-ttu-id="3324f-112">Объект **Recordset** типа Dynaset является динамическим набором записей, которые можно использовать для добавления, изменения и удаления записей из базовой таблицы базы данных или таблиц.</span><span class="sxs-lookup"><span data-stu-id="3324f-112">A dynaset-type **Recordset** object is a dynamic set of records that you can use to add, change, or delete records from an underlying database table or tables.</span></span> <span data-ttu-id="3324f-113">Объект **Recordset** типа Dynaset может содержать поля из одной или нескольких таблиц в базе данных.</span><span class="sxs-lookup"><span data-stu-id="3324f-113">A dynaset-type **Recordset** object can contain fields from one or more tables in a database.</span></span> <span data-ttu-id="3324f-114">Этот тип соответствует курсору набор ключей ODBC.</span><span class="sxs-lookup"><span data-stu-id="3324f-114">This type corresponds to an ODBC keyset cursor.</span></span>

- <span data-ttu-id="3324f-115">Объект Recordset типа моментальный снимок — статическая копия набора записей, которую можно использовать для поиска данных или создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="3324f-115">Snapshot-type Recordset— a static copy of a set of records that you can use to find data or generate reports.</span></span> <span data-ttu-id="3324f-116">Объект **Recordset** типа моментальный снимок может содержать поля из одной или нескольких таблиц в базе данных, но не может обновляться.</span><span class="sxs-lookup"><span data-stu-id="3324f-116">A snapshot-type **Recordset** object can contain fields from one or more tables in a database but can't be updated.</span></span> <span data-ttu-id="3324f-117">Этот тип соответствует статическому курсору ODBC.</span><span class="sxs-lookup"><span data-stu-id="3324f-117">This type corresponds to an ODBC static cursor.</span></span>

- <span data-ttu-id="3324f-118">Объект Recordset однонаправленного типа — аналогичен моментальному снимку с единственной разницей в отсутствии курсора.</span><span class="sxs-lookup"><span data-stu-id="3324f-118">Forward-only-type Recordset— identical to a snapshot except that no cursor is provided.</span></span> <span data-ttu-id="3324f-119">Вы можете только прокручивать записи вперед.</span><span class="sxs-lookup"><span data-stu-id="3324f-119">You can only scroll forward through records.</span></span> <span data-ttu-id="3324f-120">Это повышает производительность в ситуациях, где достаточно только один раз просмотреть итоговый набор.</span><span class="sxs-lookup"><span data-stu-id="3324f-120">This improves performance in situations where you only need to make a single pass through a result set.</span></span> <span data-ttu-id="3324f-121">Этот тип соответствует однонаправленному курсору ODBC.</span><span class="sxs-lookup"><span data-stu-id="3324f-121">This type corresponds to an ODBC forward-only cursor.</span></span>

- <span data-ttu-id="3324f-122">Динамический тип объекта Recordset — набор результатов запроса, получаемый из одной или нескольких базовых таблиц, в котором вы можете добавить, изменить или удалить записи из возвращающего строку запроса.</span><span class="sxs-lookup"><span data-stu-id="3324f-122">Dynamic-type Recordset— a query result set from one or more base tables in which you can add, change, or delete records from a row-returning query.</span></span> <span data-ttu-id="3324f-123">Кроме того, записи, которые добавляют, удаляют или изменяют другие пользователи в базовой таблице, также будут отображаться в вашем объекте **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3324f-123">Further, records other users add, delete, or edit in the base tables also appear in your **Recordset**.</span></span> <span data-ttu-id="3324f-124">Этот тип соответствует динамическому курсору ODBC (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="3324f-124">This type corresponds to an ODBC dynamic cursor (ODBCDirect workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="3324f-125">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3324f-125">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3324f-126">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3324f-126">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="3324f-127">Вы можете выбрать тип объекта **Recordset**, который вы хотите создать, с помощью аргумента типа метода **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="3324f-127">You can choose the type of **Recordset** object you want to create using the type argument of the **OpenRecordset** method.</span></span>

<span data-ttu-id="3324f-128">В рабочей области Microsoft Access, если не задан тип, интерфейс DAO пытается создать тип объекта**Recordset** с наиболее широким набором функций, начиная с табличного.</span><span class="sxs-lookup"><span data-stu-id="3324f-128">In a Microsoft Access workspace, if you don't specify a type, DAO attempts to create the type of **Recordset** with the most functionality available, starting with table.</span></span> <span data-ttu-id="3324f-129">Если этот тип не поддерживается, интерфейс DAO пытается создать объект типа Dynaset, затем моментальный снимок и, наконец, однонаправленный тип объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3324f-129">If this type isn't available, DAO attempts a dynaset, then a snapshot, and finally a forward-only type **Recordset** object.</span></span>

<span data-ttu-id="3324f-130">В рабочей области ODBCDirect, если не задан тип, интерфейс DAO пытается создать тип объекта**Recordset** с самой быстрой реакцией на запрос, начиная с однонаправленного типа.</span><span class="sxs-lookup"><span data-stu-id="3324f-130">In an ODBCDirect workspace, if you don't specify a type, DAO attempts to create the type of **Recordset** with the fastest query response, starting with forward-only.</span></span> <span data-ttu-id="3324f-131">Если этот тип не поддерживается, интерфейс DAO пытается создать объект типа мгновенный снимок, затем dynaset и, наконец, динамический тип объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3324f-131">If this type isn't available, DAO attempts a snapshot, then a dynaset, and finally a dynamic- type **Recordset** object.</span></span>

<span data-ttu-id="3324f-132">При создании объекта **Recordset** с помощью несвязанного объекта \*\* [TableDef](tabledef-object-dao.md) \*\* в рабочей области Microsoft Access, создается табличный тип объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3324f-132">When creating a **Recordset** object using a non-linked **[TableDef](tabledef-object-dao.md)** object in a Microsoft Access workspace, table-type **Recordset** objects are created.</span></span> <span data-ttu-id="3324f-133">Только объекты **Recordset** динамического типа или типа моментальный снимок могут создаваться со связанными таблицами или таблицами в базах данных ODBC с подключенным ядром СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3324f-133">Only dynaset-type or snapshot-type **Recordset** objects can be created with linked tables or tables in Microsoft Access database engine-connected ODBC databases.</span></span>

<span data-ttu-id="3324f-134">Объект **Recordset** автоматически добавляется в коллекцию **Recordsets** при открытии объекта и автоматически удаляется при его закрытии.</span><span class="sxs-lookup"><span data-stu-id="3324f-134">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the object, and is automatically removed when you close it.</span></span>

> [!NOTE]
> <span data-ttu-id="3324f-135">Если вы используете переменные для представления объекта **Recordset** и объекта **Database**, который содержит объект **Recordset**, убедитесь, что переменные принадлежат к той же области или имеют то же время существования.</span><span class="sxs-lookup"><span data-stu-id="3324f-135">If you use variables to represent a **Recordset** object and the **Database** object that contains the **Recordset**, make sure the variables have the same scope, or lifetime.</span></span> <span data-ttu-id="3324f-136">Например, если вы объявляете публичную переменную, которая определяет объект **Recordset**, убедитесь, что переменная, которая представляет **Database** с **Recordset**, также является публичной, или объявлена с помощью процедуры **Sub** или **Function** с применением ключевого слова **Static**.</span><span class="sxs-lookup"><span data-stu-id="3324f-136">For example, if you declare a public variable that represents a **Recordset** object, make sure the variable that represents the **Database** containing the **Recordset** is also public, or is declared in a **Sub** or **Function** procedure using the **Static** keyword.</span></span>

<span data-ttu-id="3324f-137">Вы можете создать любое количество переменных объекта **Recordset** при необходимости.</span><span class="sxs-lookup"><span data-stu-id="3324f-137">You can create as many **Recordset** object variables as needed.</span></span> <span data-ttu-id="3324f-138">Различные объекты **Recordset** могут получать доступ к одним таблицам, запросам и полям без возникновения конфликта.</span><span class="sxs-lookup"><span data-stu-id="3324f-138">Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="3324f-139">Типы Dynaset, моментальный снимок и однонаправленный для объекта **Recordset** хранятся в локальной памяти.</span><span class="sxs-lookup"><span data-stu-id="3324f-139">Dynaset–, snapshot–, and forward–only–type **Recordset** objects are stored in local memory.</span></span> <span data-ttu-id="3324f-140">Если в локальной памяти для хранения данных недостаточно места, ядро СУБД Microsoft Access сохраняет дополнительные данные в дисковом пространстве TEMP.</span><span class="sxs-lookup"><span data-stu-id="3324f-140">If there isn't enough space in local memory to store the data, the Microsoft Access database engine saves the additional data to TEMP disk space.</span></span> <span data-ttu-id="3324f-141">Если свободное место заканчивается, возникает перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="3324f-141">If this space is exhausted, a trappable error occurs.</span></span>

<span data-ttu-id="3324f-142">По умолчанию для объекта **Recordset** используется коллекция **Поля**, а используемым по умолчанию свойством объекта \*\* [Поле](field-object-dao.md) \*\* является свойство\*\* [Значение](field-value-property-dao.md) \*\*.</span><span class="sxs-lookup"><span data-stu-id="3324f-142">The default collection of a **Recordset** object is the **Fields** collection, and the default property of a **[Field](field-object-dao.md)** object is the **[Value](field-value-property-dao.md)** property.</span></span> <span data-ttu-id="3324f-143">Используйте эти настройки по умолчанию для упрощения вашего кода.</span><span class="sxs-lookup"><span data-stu-id="3324f-143">Use these defaults to simplify your code.</span></span>

<span data-ttu-id="3324f-144">При создании объекта **Recordset** текущая запись расположена по направлению к первой записью, если есть какие-либо записи.</span><span class="sxs-lookup"><span data-stu-id="3324f-144">When you create a **Recordset** object, the current record is positioned to the first record if there are any records.</span></span> <span data-ttu-id="3324f-145">Если записи отсутствуют, свойство **RecordCount** имеет значение 0, а свойство **BOF** и **EOF** имеют значение **ИСТИНА**.</span><span class="sxs-lookup"><span data-stu-id="3324f-145">If there are no records, the **RecordCount** property setting is 0, and the **BOF** and **EOF** property settings are **True**.</span></span>

<span data-ttu-id="3324f-146">Вы можете использовать методы **MoveNext**, **MovePrevious**, **MoveFirst** и **MoveLast**, чтобы изменить положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3324f-146">You can use the **MoveNext**, **MovePrevious**, **MoveFirst**, and **MoveLast** methods to reposition the current record.</span></span> <span data-ttu-id="3324f-147">Объекты **Recordset** однонаправленного типа поддерживают только метод **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="3324f-147">Forward–only–type **Recordset** objects support only the **MoveNext** method.</span></span> <span data-ttu-id="3324f-148">При использовании методов перемещения для перехода к каждой записи (или «прогулки» по объекту **Recordset**), вы можете использовать свойства **BOF** и **EOF**, чтобы проверить начало или конец объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3324f-148">When using the Move methods to visit each record (or "walk" through the **Recordset**), you can use the **BOF** and **EOF** properties to check for the beginning or end of the **Recordset** object.</span></span>

<span data-ttu-id="3324f-149">Для объектов **Recordset** типа dynaset и моментальный список в рабочей области Microsoft Access можно также использовать методы поиска, например **FindFirst**, чтобы найти определенную запись на основе критериев.</span><span class="sxs-lookup"><span data-stu-id="3324f-149">With dynaset- and snapshot-type **Recordset** objects in a Microsoft Access workspace, you can also use the Find methods, such as **FindFirst**, to locate a specific record based on criteria.</span></span> <span data-ttu-id="3324f-150">Если запись не найдена, свойство **NoMatch** получает значение **ИСТИНА**.</span><span class="sxs-lookup"><span data-stu-id="3324f-150">If the record isn't found, the **NoMatch** property is set to **True**.</span></span> <span data-ttu-id="3324f-151">Для табличного типа объектов **Recordset** можно сканировать записи, используя метод **Seek**.</span><span class="sxs-lookup"><span data-stu-id="3324f-151">For table-type **Recordset** objects, you can scan records using the **Seek** method.</span></span>

<span data-ttu-id="3324f-152">Свойство **Type** указывает тип созданного объекта **Recordset**, а свойство **Updatable** указывает на то, можете ли вы изменить записи объекта.</span><span class="sxs-lookup"><span data-stu-id="3324f-152">The **Type** property indicates the type of **Recordset** object created, and the **Updatable** property indicates whether you can change the object's records.</span></span>

<span data-ttu-id="3324f-153">Сведения о структуре базовой таблицы, например, имена и типы данных каждого объекта **Field** и любых объектов **Index** хранятся в объекте **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="3324f-153">Information about the structure of a base table, such as the names and data types of each **Field** object and any **Index** objects, is stored in a **TableDef** object.</span></span>

<span data-ttu-id="3324f-154">Чтобы сослаться на объект **Recordset** в коллекции по его порядковому номеру или по его свойству**Name**, используйте любую из следующих синтаксических форм:</span><span class="sxs-lookup"><span data-stu-id="3324f-154">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="3324f-155">**Recordsets**(0)</span><span class="sxs-lookup"><span data-stu-id="3324f-155">**Recordsets**(0)</span></span>

- <span data-ttu-id="3324f-156">**Recordsets**("name")</span><span class="sxs-lookup"><span data-stu-id="3324f-156">**Recordsets**("name")</span></span>

- <span data-ttu-id="3324f-157">**Recordsets**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="3324f-157">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="3324f-158">Вы можете открыть объект **Recordset** из одного источника данных или базы данных несколько раз, создавая дублирующие имена в коллекции **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="3324f-158">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection.</span></span> <span data-ttu-id="3324f-159">Вы должны назначить объекты **Recordsets** для переменных объекта и ссылаться на них по имени переменной.</span><span class="sxs-lookup"><span data-stu-id="3324f-159">You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="3324f-160">Пример</span><span class="sxs-lookup"><span data-stu-id="3324f-160">Example</span></span>

<span data-ttu-id="3324f-161">В этом примере показаны объекты **Recordset** и коллекция \*\*Recordset \*\* с помощью открытия четырех разных типов **Recordsets**, перечисления коллекции Recordsets для текущего объекта **Database**и перечисления коллекции **Properties** для каждого объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3324f-161">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

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

В этом примере используется метод**OpenRecordset** для открытия пяти разных объектов **Recordset** и отображения их содержимого. <span data-ttu-id="3324f-163">Процедура OpenRecordsetOutput является обязательной для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="3324f-163">The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="3324f-164">В этом примере открывается динамический тип объекта **Recordset** и перечисляются ее записи.</span><span class="sxs-lookup"><span data-stu-id="3324f-164">This example opens a dynamic-type **Recordset** object and enumerates its records.</span></span>

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

<span data-ttu-id="3324f-165">В этом примере открывается тип dynaset объекта **Recordset** и отображаются уровни обновления его полей.</span><span class="sxs-lookup"><span data-stu-id="3324f-165">This example opens a dynaset-type **Recordset** and shows the extent to which its fields are updatable.</span></span>

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

<span data-ttu-id="3324f-166">В этом примере открывается однонаправленный тип объекта **Recordset**, демонстрируются характеристики только для чтения и пошаговые инструкции для объекта **Recordset** и метода **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="3324f-166">This example opens a forward-only-type **Recordset**, demonstrates its read-only characteristics, and steps through the **Recordset** with the **MoveNext** method.</span></span>

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

<span data-ttu-id="3324f-167">В этом примере открывается тип моментальный снимок объекта **Recordset** и демонстрируются характеристики только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3324f-167">This example opens a snapshot-type **Recordset** and demonstrates its read-only characteristics.</span></span>

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

<span data-ttu-id="3324f-168">В этом примере открывается табличный тип объекта **Recordset**, задается его свойство **Index** и перечисляются его записи.</span><span class="sxs-lookup"><span data-stu-id="3324f-168">This example opens a table-type **Recordset**, sets its **Index** property, and enumerates its records.</span></span>

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

<span data-ttu-id="3324f-169">В приведенном ниже примере показано, как использовать метод Seek для поиска записи в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="3324f-169">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="3324f-170">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="3324f-170">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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

<span data-ttu-id="3324f-171">В приведенном ниже примере показано, как открыть объект Recordset на основании запроса параметра.</span><span class="sxs-lookup"><span data-stu-id="3324f-171">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

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

<span data-ttu-id="3324f-172">В приведенном ниже примере показано, как открыть объект Recordset на основании таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="3324f-172">The following example shows how to open a Recordset based on a table or a query.</span></span>

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

<span data-ttu-id="3324f-173">В приведенном ниже примере показано, как открыть объект Recordset на основании SQL оператора.</span><span class="sxs-lookup"><span data-stu-id="3324f-173">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

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

<span data-ttu-id="3324f-174">В приведенном ниже примере показано, как использовать методы FindFirst и FindNext для поиска записи в Recordset.</span><span class="sxs-lookup"><span data-stu-id="3324f-174">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

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

<span data-ttu-id="3324f-175">В приведенном ниже примере показано, как скопировать результаты запроса на лист в новой книге Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3324f-175">The following example shows how to copy the results of a query to a worksheet in a new Microsoft Excel workbook.</span></span>

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

