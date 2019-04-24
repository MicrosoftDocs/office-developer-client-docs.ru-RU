---
title: Свойство Recordset. CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: 8632f5fb-6e5d-5a3e-1bd7-81e1270e9531
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196807(v=office.15)
ms:contentKeyID: 48546079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 369ff9192bb592c96e17920c9771c10b70dc233b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300597"
---
# <a name="recordsetcachesize-property-dao"></a><span data-ttu-id="fa674-102">Свойство Recordset. CacheSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="fa674-102">Recordset.CacheSize property (DAO)</span></span>


<span data-ttu-id="fa674-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa674-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa674-104">Задает или возвращает число записей, полученных из источника данных ODBC, который будет кэшироваться локально.</span><span class="sxs-lookup"><span data-stu-id="fa674-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="fa674-105">Для чтения и записи, **Long**.</span><span class="sxs-lookup"><span data-stu-id="fa674-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa674-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa674-106">Syntax</span></span>

<span data-ttu-id="fa674-107">*Expression* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="fa674-107">*expression* .CacheSize</span></span>

<span data-ttu-id="fa674-108">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fa674-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa674-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa674-109">Remarks</span></span>

<span data-ttu-id="fa674-110">Значение свойства **CacheSize** должно находиться в пределах от 5 до 1200, но не больше, чем доступная память.</span><span class="sxs-lookup"><span data-stu-id="fa674-110">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow.</span></span> <span data-ttu-id="fa674-111">Типичное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="fa674-111">A typical value is 100.</span></span> <span data-ttu-id="fa674-112">Значение 0 отключает кэширование.</span><span class="sxs-lookup"><span data-stu-id="fa674-112">A setting of 0 turns off caching.</span></span>

<span data-ttu-id="fa674-113">Кэширование данных повышает производительность, если вы используете объекты **Recordset** для получения данных с удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="fa674-113">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server.</span></span> <span data-ttu-id="fa674-114">Кэш — это пространство в локальной памяти, в котором хранятся данные, которые были получены последними с сервера. Это полезно, если пользователи запрашивают данные еще раз во время выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="fa674-114">A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running.</span></span> <span data-ttu-id="fa674-115">Когда пользователи запрашивают данные, ядро СУБД Microsoft Access сначала проверяет кэш для запрошенных данных, а не извлекает его с сервера, что занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="fa674-115">When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time.</span></span> <span data-ttu-id="fa674-116">Кэш сохраняет данные, поступающие из источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="fa674-116">The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="fa674-117">Любой источник данных ODBC, подключенный к ядру СУБД Microsoft Access (например, связанная таблица), может иметь локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="fa674-117">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache.</span></span> <span data-ttu-id="fa674-118">Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, задайте свойства **CacheSize** и **[CacheStart](recordset-cachestart-property-dao.md)** , а затем используйте метод **[FillCache](recordset-fillcache-method-dao.md)** или Пошаговое перемещение записей с помощью методов **Move** .</span><span class="sxs-lookup"><span data-stu-id="fa674-118">To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="fa674-119">Вы можете создать значение свойства **CacheSize** для количества записей, обрабатываемых приложением одновременно.</span><span class="sxs-lookup"><span data-stu-id="fa674-119">You can base the **CacheSize** property setting on the number of records your application can handle at one time.</span></span> <span data-ttu-id="fa674-120">Например, если вы используете объект **Recordset** в качестве источника данных, которые будут отображаться на экране, можно установить для свойства **CacheSize** значение 20, чтобы отобразить 20 записей за один раз.</span><span class="sxs-lookup"><span data-stu-id="fa674-120">For example, if you're using a **Recordset** object as the source of the data to be displayed on screen, you could set its **CacheSize** property to 20 to display 20 records at one time.</span></span>

<span data-ttu-id="fa674-121">Ядро СУБД Microsoft Access запрашивает записи в диапазоне кэша из кэша и запрашивает записи за пределами диапазона кэша с сервера.</span><span class="sxs-lookup"><span data-stu-id="fa674-121">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="fa674-122">Записи, извлеченные из кэша, не отражают параллельные изменения, внесенные другими пользователями в исходные данные.</span><span class="sxs-lookup"><span data-stu-id="fa674-122">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

<span data-ttu-id="fa674-123">Чтобы принудительно обновить все кэшированные данные, задайте для свойства **CacheSize** объекта **Recordset** значение 0, повторно задайте для него размер кэша, который вы изначально запросили, а затем используйте метод **FillCache** .</span><span class="sxs-lookup"><span data-stu-id="fa674-123">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

## <a name="example"></a><span data-ttu-id="fa674-124">Пример</span><span class="sxs-lookup"><span data-stu-id="fa674-124">Example</span></span>

<span data-ttu-id="fa674-125">В этом примере используются методы **CreateTableDef** и **FillCache** и свойства **CacheSize**, **CacheStart** и **SourceTableName** для перечисления записей в связанной таблице два раза.</span><span class="sxs-lookup"><span data-stu-id="fa674-125">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice.</span></span> <span data-ttu-id="fa674-126">Затем выполняется перечисление дважды с кэшем в 50 записей.</span><span class="sxs-lookup"><span data-stu-id="fa674-126">Then it enumerates the records twice with a 50-record cache.</span></span> <span data-ttu-id="fa674-127">Затем пример отображает статистику производительности для некэшированных и кэшированных запусков в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="fa674-127">The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
