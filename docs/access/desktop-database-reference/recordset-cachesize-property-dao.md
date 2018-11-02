---
title: Свойство Recordset.CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: 8632f5fb-6e5d-5a3e-1bd7-81e1270e9531
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196807(v=office.15)
ms:contentKeyID: 48546079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3a337226d0b710394469649c0846d92b079b2ed
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924829"
---
# <a name="recordsetcachesize-property-dao"></a><span data-ttu-id="d7896-102">Свойство Recordset.CacheSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="d7896-102">Recordset.CacheSize property (DAO)</span></span>


<span data-ttu-id="d7896-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7896-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7896-104">Задает или возвращает число записей, полученных из источника данных ODBC, которые будут кэшированы локально.</span><span class="sxs-lookup"><span data-stu-id="d7896-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="d7896-105">Чтение и запись **времени**.</span><span class="sxs-lookup"><span data-stu-id="d7896-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7896-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7896-106">Syntax</span></span>

<span data-ttu-id="d7896-107">*выражение* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="d7896-107">*expression* .CacheSize</span></span>

<span data-ttu-id="d7896-108">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="d7896-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7896-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="d7896-109">Remarks</span></span>

<span data-ttu-id="d7896-110">Значение свойства **CacheSize** должен быть между 5 и 1200, но не больше, чем объем доступной памяти будет разрешено.</span><span class="sxs-lookup"><span data-stu-id="d7896-110">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow.</span></span> <span data-ttu-id="d7896-111">Стандартное значение равно 100.</span><span class="sxs-lookup"><span data-stu-id="d7896-111">A typical value is 100.</span></span> <span data-ttu-id="d7896-112">Значение 0 отключает кэширование.</span><span class="sxs-lookup"><span data-stu-id="d7896-112">A setting of 0 turns off caching.</span></span>

<span data-ttu-id="d7896-113">Кэширование данных улучшает производительность при использовании **набора записей** объектов для извлечения данных из удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="d7896-113">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server.</span></span> <span data-ttu-id="d7896-114">Кэш — это должен быть пробел в локальной памяти, в которой содержатся данные, недавно извлеченные с сервера. Это полезно, если пользователи запрашивать данные еще раз во время выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="d7896-114">A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running.</span></span> <span data-ttu-id="d7896-115">Когда пользователь запрашивает данные, ядро базы данных Microsoft Access кэша для запрошенные данные сначала проверяет вместо извлечение из сервера, который занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="d7896-115">When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time.</span></span> <span data-ttu-id="d7896-116">Кэш сохраняет только данные, поступающие из источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="d7896-116">The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="d7896-117">Любой Microsoft Access базы данных подключением модуль ODBC источник данных, например связанной таблицы может иметь локального кэша.</span><span class="sxs-lookup"><span data-stu-id="d7896-117">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache.</span></span> <span data-ttu-id="d7896-118">Создание кэша, откройте объект **набора записей** из к удаленному источнику данных, задать свойства **CacheSize** и **[CacheStart](recordset-cachestart-property-dao.md)** и затем используйте метод **[FillCache](recordset-fillcache-method-dao.md)** или пошаговое выполнение записи с помощью методов **перемещения** .</span><span class="sxs-lookup"><span data-stu-id="d7896-118">To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="d7896-119">Настройка свойства **CacheSize** можно создать на количество записей, приложение может обрабатывать за один раз.</span><span class="sxs-lookup"><span data-stu-id="d7896-119">You can base the **CacheSize** property setting on the number of records your application can handle at one time.</span></span> <span data-ttu-id="d7896-120">Например при использовании объекта **набора записей** как источник данных для отображения на экране может установите его свойство **CacheSize** 20 для отображения 20 записей одновременно.</span><span class="sxs-lookup"><span data-stu-id="d7896-120">For example, if you're using a **Recordset** object as the source of the data to be displayed on screen, you could set its **CacheSize** property to 20 to display 20 records at one time.</span></span>

<span data-ttu-id="d7896-121">Ядро базы данных Microsoft Access запрашивает записей в диапазоне кэша из кэша и запрашивает записи вне диапазона кэша с сервера.</span><span class="sxs-lookup"><span data-stu-id="d7896-121">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="d7896-122">Записей, полученных из кэша не отражает параллельных изменений других пользователей в источник данных.</span><span class="sxs-lookup"><span data-stu-id="d7896-122">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

<span data-ttu-id="d7896-123">Чтобы принудительно выполнить обновление всех кэшированных данных, значение 0, снова задайте для него значение размера кэша, изначально запрошен, а затем использовать метод **FillCache** свойство **CacheSize** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="d7896-123">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

## <a name="example"></a><span data-ttu-id="d7896-124">Пример</span><span class="sxs-lookup"><span data-stu-id="d7896-124">Example</span></span>

<span data-ttu-id="d7896-125">В этом примере используется **CacheSize**, **CacheStart** и **SourceTableName** свойства и методы **CreateTableDef** и **FillCache** дважды перечисление записей в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="d7896-125">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice.</span></span> <span data-ttu-id="d7896-126">Затем выполняется перечисление записей дважды с 50 записи кэша.</span><span class="sxs-lookup"><span data-stu-id="d7896-126">Then it enumerates the records twice with a 50-record cache.</span></span> <span data-ttu-id="d7896-127">Затем отображается статистика производительности без кэш-памяти и кэшированные просматривает связанную таблицу.</span><span class="sxs-lookup"><span data-stu-id="d7896-127">The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
