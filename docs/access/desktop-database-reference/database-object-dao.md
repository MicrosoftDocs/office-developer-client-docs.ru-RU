---
title: Объект Database (DAO)
TOCTitle: Database Object
ms:assetid: 6cf2ddf8-3957-a15e-5eeb-85f81c1e415e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195520(v=office.15)
ms:contentKeyID: 48545482
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm0
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c23772c54f2f980b8d10d4afc352687935840752
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294842"
---
# <a name="database-object-dao"></a><span data-ttu-id="ef20d-102">Объект Database (DAO)</span><span class="sxs-lookup"><span data-stu-id="ef20d-102">Database Object (DAO)</span></span>

<span data-ttu-id="ef20d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef20d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef20d-104">Объект **Database** представляет открытую базу данных.</span><span class="sxs-lookup"><span data-stu-id="ef20d-104">A **Database** object represents an open database.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef20d-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef20d-105">Remarks</span></span>

<span data-ttu-id="ef20d-106">Объект **Database**, его методы и свойства используются для операций с открытой базы данных.</span><span class="sxs-lookup"><span data-stu-id="ef20d-106">You use the **Database** object and its methods and properties to manipulate an open database.</span></span> <span data-ttu-id="ef20d-107">В базе данных любого типа вы можете:</span><span class="sxs-lookup"><span data-stu-id="ef20d-107">With any type of database or connection, you can:</span></span>

  - <span data-ttu-id="ef20d-108">Использовать метод **Execute**, чтобы выполнить запрос на изменение.</span><span class="sxs-lookup"><span data-stu-id="ef20d-108">Use the **Execute** method to run an action query.</span></span>

  - <span data-ttu-id="ef20d-109">Задать свойство **Connect**, чтобы установить соединение с источником данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="ef20d-109">Set the **Connect** property to establish a connection to an ODBC data source.</span></span>

  - <span data-ttu-id="ef20d-110">Задать свойство **QueryTimeout**, чтобы ограничить продолжительность ожидания выполнения запроса в источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="ef20d-110">Set the **QueryTimeout** property to limit the length of time to wait for a query to execute against an ODBC data source.</span></span>

  - <span data-ttu-id="ef20d-111">Использовать свойство **RecordsAffected**, чтобы определить количество измененных записей в результате запроса на изменение.</span><span class="sxs-lookup"><span data-stu-id="ef20d-111">Use the **RecordsAffected** property to determine how many records were changed by an action query.</span></span>

  - <span data-ttu-id="ef20d-112">Использовать метод **OpenRecordset**, чтобы выполнить запрос на выборку и создать объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-112">Use the **OpenRecordset** method to execute a select query and create a **Recordset** object.</span></span>

  - <span data-ttu-id="ef20d-113">Использовать свойство **Version**, чтобы определить версию ядра СУБД, создавшую базу данных.</span><span class="sxs-lookup"><span data-stu-id="ef20d-113">Use the **Version** property to determine which version of a database engine created the database.</span></span>

<span data-ttu-id="ef20d-114">С помощью базы данных ядра СУБД Microsoft Access можно также использовать другие методы, свойства и коллекции для работы с объектом **Database**, а также создавать, изменять или получать сведения о его таблицах, запросах и отношениях.</span><span class="sxs-lookup"><span data-stu-id="ef20d-114">With a Microsoft Access database engine database, you can also use other methods, properties, and collections to manipulate a **Database** object, as well as create, modify, or get information about its tables, queries, and relationships.</span></span> <span data-ttu-id="ef20d-115">Например, вы можете:</span><span class="sxs-lookup"><span data-stu-id="ef20d-115">For example, you can:</span></span>

  - <span data-ttu-id="ef20d-116">Использовать методы **CreateTableDef** и **CreateRelation**, чтобы создавать таблицы и отношения соответственно.</span><span class="sxs-lookup"><span data-stu-id="ef20d-116">Use the **CreateTableDef** and **CreateRelation** methods to create tables and relations, respectively.</span></span>

  - <span data-ttu-id="ef20d-117">Использовать метод **CreateProperty**, чтобы определить новые свойства **Database**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-117">Use the **CreateProperty** method to define new **Database** properties.</span></span>

  - <span data-ttu-id="ef20d-118">Использовать метод **CreateQueryDef**, чтобы создать постоянное или временное определение запроса.</span><span class="sxs-lookup"><span data-stu-id="ef20d-118">Use the **CreateQueryDef** method to create a persistent or temporary query definition.</span></span>

  - <span data-ttu-id="ef20d-119">Использовать методы **MakeReplica**, **Synchronize** и **PopulatePartial**, чтобы создать и синхронизировать полные или частичные копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="ef20d-119">Use **MakeReplica**, **Synchronize**, and **PopulatePartial** methods to create and synchronize full or partial replicas of your database.</span></span>

  - <span data-ttu-id="ef20d-120">Задать свойство **CollatingOrder**, чтобы установить порядок сортировки по алфавиту для символьных полей на разных языках.</span><span class="sxs-lookup"><span data-stu-id="ef20d-120">Set the **CollatingOrder** property to establish the alphabetic sorting order for character-based fields in different languages.</span></span>

<span data-ttu-id="ef20d-121">Метод **CreateDatabase** используется для создания постоянного объекта **Database**, автоматически добавляемого в коллекцию **Databases**, что обеспечивает его сохранение на диске.</span><span class="sxs-lookup"><span data-stu-id="ef20d-121">You use the **CreateDatabase** method to create a persistent **Database** object that is automatically appended to the **Databases** collection, thereby saving it to disk.</span></span>

<span data-ttu-id="ef20d-122">Не нужно указывать объект **DBEngine** при использовании метода **OpenDatabase**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-122">You don't need to specify the **DBEngine** object when you use the **OpenDatabase** method.</span></span>

<span data-ttu-id="ef20d-123">Открытие базы данных со связанными таблицами не создает автоматически ссылки на указанные внешние файлы.</span><span class="sxs-lookup"><span data-stu-id="ef20d-123">Opening a database with linked tables doesn't automatically establish links to the specified external files.</span></span> <span data-ttu-id="ef20d-124">Необходимо либо создать ссылку на объект **TableDef** или объекты **Field** таблицы, либо открыть объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-124">You must either reference the table's **TableDef** or **Field** objects or open a **Recordset** object.</span></span> <span data-ttu-id="ef20d-125">Если не удается создать ссылки на эти таблицы, возникает перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="ef20d-125">If you can't establish links to these tables, a trappable error occurs.</span></span> <span data-ttu-id="ef20d-126">Может также требоваться разрешение на доступ к базе данных или другой пользователь мог открыть базу данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="ef20d-126">You may also need permission to access the database, or another user might have the database opened exclusively.</span></span> <span data-ttu-id="ef20d-127">В этих случаях возникают перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="ef20d-127">In these cases, trappable errors occur.</span></span>

<span data-ttu-id="ef20d-128">Когда выполнена процедура, объявляющая объект **Database**, локальные объекты **Database** закрываются вместе с любыми открытыми объектами **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-128">When a procedure that declares a **Database** object has executed, local **Database** objects are closed along with any open **Recordset** objects.</span></span> <span data-ttu-id="ef20d-129">Любые ожидающие обновления пропадают, и выполняется откат всех ожидающих транзакций, но перехватываемая ошибка не возникает.</span><span class="sxs-lookup"><span data-stu-id="ef20d-129">Any pending updates are lost and any pending transactions are rolled back, but no trappable error occurs.</span></span> <span data-ttu-id="ef20d-130">Следует явным образом завершить все ожидающие транзакции или изменения и закрыть объекты **Recordset** и **Database** перед процедурами выхода, локально объявляющими эти переменные объектов.</span><span class="sxs-lookup"><span data-stu-id="ef20d-130">You should explicitly complete any pending transactions or edits and close **Recordset** objects and **Database** objects before exiting procedures that declare these object variables locally.</span></span>

<span data-ttu-id="ef20d-131">Если вы используете один из методов транзакции (**BeginTrans**, **CommitTrans** или **Rollback**) для объекта **Workspace**, эти транзакции применяются ко всем базам данных, открытым в объекте **Workspace**, из которого был открыт объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-131">When you use one of the transaction methods (**BeginTrans**, **CommitTrans**, or **Rollback**) on the **Workspace** object, these transactions apply to all databases opened on the **Workspace** from which the **Database** object was opened.</span></span> <span data-ttu-id="ef20d-132">Если нужно использовать независимые транзакции, необходимо сначала открыть дополнительный объект **Workspace**, а затем открыть другой объект **Database** в этом объекте **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-132">If you want to use independent transactions, you must first open an additional **Workspace** object, and then open another **Database** object in that **Workspace** object.</span></span>


> [!NOTE]
> <span data-ttu-id="ef20d-133">Вы можете открывать один источник данных или базу данных несколько раз, создавая дублирующие имена в коллекции **Databases**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-133">You can open a Recordset object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection.</span></span> <span data-ttu-id="ef20d-134">Вы должны назначить объекты **Database** для переменных объекта и ссылаться на них по имени переменной.</span><span class="sxs-lookup"><span data-stu-id="ef20d-134">You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>



## <a name="example"></a><span data-ttu-id="ef20d-135">Пример</span><span class="sxs-lookup"><span data-stu-id="ef20d-135">Example</span></span>

<span data-ttu-id="ef20d-136">В этом примере создается новый объект **Database** и открывается существующий объект **Database** в объекте **Workspace**, используемом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef20d-136">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object.</span></span> <span data-ttu-id="ef20d-137">Затем выполняется перечисление коллекции **Database** и коллекции **Properties** каждого объекта **Database**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-137">Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccessWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="ef20d-138">В этом примере используется метод **CreateDatabase** для создания нового зашифрованного объекта **Database**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-138">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```
