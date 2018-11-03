---
title: Объект базы данных (DAO)
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
ms.openlocfilehash: 265edf6b5d426b87d718c66e9886b7a4877120de
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918851"
---
# <a name="database-object-dao"></a><span data-ttu-id="fb768-102">Объект базы данных (DAO)</span><span class="sxs-lookup"><span data-stu-id="fb768-102">Database object (DAO)</span></span>

<span data-ttu-id="fb768-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb768-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb768-104">Объект **базы данных** представляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="fb768-104">A **Database** object represents an open database.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb768-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="fb768-105">Remarks</span></span>

<span data-ttu-id="fb768-106">Используйте объект **базы данных** и его методы и свойства для работы с открытой базы данных.</span><span class="sxs-lookup"><span data-stu-id="fb768-106">You use the **Database** object and its methods and properties to manipulate an open database.</span></span> <span data-ttu-id="fb768-107">В базе данных любого типа можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb768-107">In any type of database, you can:</span></span>

  - <span data-ttu-id="fb768-108">Метод **Execute** для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="fb768-108">Use the **Execute** method to run an action query.</span></span>

  - <span data-ttu-id="fb768-109">Присвойте свойству **подключение** для установления подключения к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="fb768-109">Set the **Connect** property to establish a connection to an ODBC data source.</span></span>

  - <span data-ttu-id="fb768-110">Присвойте свойству **QueryTimeout** , чтобы ограничить время ожидания для запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="fb768-110">Set the **QueryTimeout** property to limit the length of time to wait for a query to execute against an ODBC data source.</span></span>

  - <span data-ttu-id="fb768-111">Свойство **RecordsAffected** позволяет определить, сколько записей были изменены с запроса.</span><span class="sxs-lookup"><span data-stu-id="fb768-111">Use the **RecordsAffected** property to determine how many records were changed by an action query.</span></span>

  - <span data-ttu-id="fb768-112">Используйте метод **OpenRecordset** для выполнения запроса и создания объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="fb768-112">Use the **OpenRecordset** method to execute a select query and create a **Recordset** object.</span></span>

  - <span data-ttu-id="fb768-113">Используйте свойство **Version** для определения, какая версия ядра базы данных создана база данных.</span><span class="sxs-lookup"><span data-stu-id="fb768-113">Use the **Version** property to determine which version of a database engine created the database.</span></span>

<span data-ttu-id="fb768-114">С базой данных ядра базы данных Microsoft Access можно также использовать другие методы, свойства и семейств сайтов для работы с объекта **базы данных** , а также создавать, изменять и получать сведения о его таблицы, запросы и связи.</span><span class="sxs-lookup"><span data-stu-id="fb768-114">With a Microsoft Access database engine database, you can also use other methods, properties, and collections to manipulate a **Database** object, as well as create, modify, or get information about its tables, queries, and relationships.</span></span> <span data-ttu-id="fb768-115">Например можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb768-115">For example, you can:</span></span>

  - <span data-ttu-id="fb768-116">Используйте методы **CreateTableDef** и **CreateRelation** для создания таблицы и связи, соответственно.</span><span class="sxs-lookup"><span data-stu-id="fb768-116">Use the **CreateTableDef** and **CreateRelation** methods to create tables and relations, respectively.</span></span>

  - <span data-ttu-id="fb768-117">Используйте метод **CreateProperty** для определения нового свойства **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="fb768-117">Use the **CreateProperty** method to define new **Database** properties.</span></span>

  - <span data-ttu-id="fb768-118">Используйте метод **CreateQueryDef** для создания определения постоянной или временной запроса.</span><span class="sxs-lookup"><span data-stu-id="fb768-118">Use the **CreateQueryDef** method to create a persistent or temporary query definition.</span></span>

  - <span data-ttu-id="fb768-119">Используйте методы **MakeReplica**, **Синхронизация**и **PopulatePartial** для создания и синхронизации реплик полное или частичное базы данных.</span><span class="sxs-lookup"><span data-stu-id="fb768-119">Use **MakeReplica**, **Synchronize**, and **PopulatePartial** methods to create and synchronize full or partial replicas of your database.</span></span>

  - <span data-ttu-id="fb768-120">Присвойте свойству **CollatingOrder** для установления буквам и цифрам порядка сортировки для текстового поля на разных языках.</span><span class="sxs-lookup"><span data-stu-id="fb768-120">Set the **CollatingOrder** property to establish the alphabetic sorting order for character-based fields in different languages.</span></span>

<span data-ttu-id="fb768-121">Используйте метод **CreateDatabase** Создание сохраняемого объекта **базы данных** , который автоматически добавляется к коллекции **баз данных** , таким образом, сохраните его на диске.</span><span class="sxs-lookup"><span data-stu-id="fb768-121">You use the **CreateDatabase** method to create a persistent **Database** object that is automatically appended to the **Databases** collection, thereby saving it to disk.</span></span>

<span data-ttu-id="fb768-122">При использовании метода **OpenDatabase** указать объект **DBEngine** не требуется.</span><span class="sxs-lookup"><span data-stu-id="fb768-122">You don't need to specify the **DBEngine** object when you use the **OpenDatabase** method.</span></span>

<span data-ttu-id="fb768-123">Открытие базы данных в связанных таблицах не устанавливать автоматически ссылки на указанные внешние файлы.</span><span class="sxs-lookup"><span data-stu-id="fb768-123">Opening a database with linked tables doesn't automatically establish links to the specified external files.</span></span> <span data-ttu-id="fb768-124">Необходимо ссылок на объекты **TableDef** или **поля** в таблице или открывает объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="fb768-124">You must either reference the table's **TableDef** or **Field** objects or open a **Recordset** object.</span></span> <span data-ttu-id="fb768-125">Если не удается установить ссылки на эти таблицы, то перехватываемые возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="fb768-125">If you can't establish links to these tables, a trappable error occurs.</span></span> <span data-ttu-id="fb768-126">Может также потребоваться разрешение на доступ к базе данных или другой пользователь может быть база данных, открыть в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="fb768-126">You may also need permission to access the database, or another user might have the database opened exclusively.</span></span> <span data-ttu-id="fb768-127">В таких случаях перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="fb768-127">In these cases, trappable errors occur.</span></span>

<span data-ttu-id="fb768-128">При выполнении процедуры, которая объявляет объекта **базы данных** и все открытые объекты **набора записей** закрываются локальных объектов **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="fb768-128">When a procedure that declares a **Database** object has executed, local **Database** objects are closed along with any open **Recordset** objects.</span></span> <span data-ttu-id="fb768-129">Все ожидающие обновления не сохраняются все ожидающие транзакции будет выполнен откат, а перехватываемые ошибка не происходит.</span><span class="sxs-lookup"><span data-stu-id="fb768-129">Any pending updates are lost and any pending transactions are rolled back, but no trappable error occurs.</span></span> <span data-ttu-id="fb768-130">Необходимо явно завершения любой транзакций в состоянии ожидания или изменения и закройте **записей** и объекты **базы данных** перед выходом из процедуры, которые работают эти данными локально.</span><span class="sxs-lookup"><span data-stu-id="fb768-130">You should explicitly complete any pending transactions or edits and close **Recordset** objects and **Database** objects before exiting procedures that declare these object variables locally.</span></span>

<span data-ttu-id="fb768-131">При использовании одного из методов транзакций (**BeginTrans**, **CommitTrans**или **отката**) на объекте **рабочей области для** этих операций применяются ко всем базам данных, открытых в **рабочей области** , из которой базе **базы данных** объект был открыт.</span><span class="sxs-lookup"><span data-stu-id="fb768-131">When you use one of the transaction methods (**BeginTrans**, **CommitTrans**, or **Rollback**) on the **Workspace** object, these transactions apply to all databases opened on the **Workspace** from which the **Database** object was opened.</span></span> <span data-ttu-id="fb768-132">Если вы хотите использовать независимых транзакций, необходимо сначала открыть дополнительные объекта **рабочей области** и откройте другой объект **базы данных** в **рабочей области для** объекта.</span><span class="sxs-lookup"><span data-stu-id="fb768-132">If you want to use independent transactions, you must first open an additional **Workspace** object, and then open another **Database** object in that **Workspace** object.</span></span>


> [!NOTE]
> <span data-ttu-id="fb768-133">Можно открыть один и тот же источник данных или базы данных более одного раза, Создание повторяющихся имен в семействе **баз данных** .</span><span class="sxs-lookup"><span data-stu-id="fb768-133">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection.</span></span> <span data-ttu-id="fb768-134">Следует назначать объектных переменных объектов **базы данных** и обращаться к ним с именем переменной.</span><span class="sxs-lookup"><span data-stu-id="fb768-134">You should assign **Database** objects to object variables and refer to them by variable name.</span></span>



## <a name="example"></a><span data-ttu-id="fb768-135">Пример</span><span class="sxs-lookup"><span data-stu-id="fb768-135">Example</span></span>

<span data-ttu-id="fb768-136">В этом примере создается новый объект **базы данных** и открывает существующий объект **базы данных** в объекте **рабочей области** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb768-136">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object.</span></span> <span data-ttu-id="fb768-137">Затем перечисляет набор **баз данных** и коллекции **свойств** каждого объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="fb768-137">Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

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

<span data-ttu-id="fb768-138">В этом примере используется **CreateDatabase** для создания нового, зашифрованные объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="fb768-138">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
