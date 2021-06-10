---
title: Свойство Recordset2.CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: d8d195cc-6696-0583-31eb-b9988f8b7c6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835090(v=office.15)
ms:contentKeyID: 48548042
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052927
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 94453b5bd8f5a405c5ad5b7c8a175468df2adfa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307429"
---
# <a name="recordset2cachesize-property-dao"></a><span data-ttu-id="a9f74-102">Свойство Recordset2.CacheSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="a9f74-102">Recordset2.CacheSize property (DAO)</span></span>


<span data-ttu-id="a9f74-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9f74-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9f74-104">Задает или возвращает число записей, полученных из источника данных ODBC, который будет кэшироваться локально.</span><span class="sxs-lookup"><span data-stu-id="a9f74-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="a9f74-105">Для чтения и записи, **Long**.</span><span class="sxs-lookup"><span data-stu-id="a9f74-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9f74-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9f74-106">Syntax</span></span>

<span data-ttu-id="a9f74-107">*выражения* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="a9f74-107">*expression* .CacheSize</span></span>

<span data-ttu-id="a9f74-108">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="a9f74-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9f74-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="a9f74-109">Remarks</span></span>

<span data-ttu-id="a9f74-110">Значение свойства **CacheSize** должно быть от 5 до 1200, но не больше, чем позволяет доступная память.</span><span class="sxs-lookup"><span data-stu-id="a9f74-110">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow.</span></span> <span data-ttu-id="a9f74-111">Обычное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="a9f74-111">A typical value is 100.</span></span> <span data-ttu-id="a9f74-112">Параметр 0 отключит кэшинг.</span><span class="sxs-lookup"><span data-stu-id="a9f74-112">A setting of 0 turns off caching.</span></span>

<span data-ttu-id="a9f74-113">Кэшинг данных повышает производительность при использовании объектов **Recordset** для получения данных с удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="a9f74-113">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server.</span></span> <span data-ttu-id="a9f74-114">Кэш — это пространство в локальной памяти, которое содержит данные, полученные с сервера; это полезно, если пользователи снова запрашивают данные во время работы приложения.</span><span class="sxs-lookup"><span data-stu-id="a9f74-114">A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running.</span></span> <span data-ttu-id="a9f74-115">При запросе данных пользователи сначала проверяют кэш для запрашиваемой информации, а не отбирают их с сервера, что занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="a9f74-115">When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time.</span></span> <span data-ttu-id="a9f74-116">Кэш сохраняет только данные, которые приходят из источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="a9f74-116">The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="a9f74-117">Любой источник данных базы данных Microsoft Access, подключенный к базе данных ODBC, например связанная таблица, может иметь локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="a9f74-117">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache.</span></span> <span data-ttu-id="a9f74-118">Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, установите свойства **CacheSize** и **[CacheStart,](recordset2-cachestart-property-dao.md)** а затем используйте метод **[FillCache](recordset2-fillcache-method-dao.md)** или перешагите записи с помощью методов **Move.**</span><span class="sxs-lookup"><span data-stu-id="a9f74-118">To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="a9f74-119">Параметр свойства **CacheSize** можно использовать в зависимости от количества записей, которые приложение может обрабатывать одновременно.</span><span class="sxs-lookup"><span data-stu-id="a9f74-119">You can base the **CacheSize** property setting on the number of records your application can handle at one time.</span></span> <span data-ttu-id="a9f74-120">Например, если вы используете объект **Recordset** в качестве источника данных, отображаемого на экране, вы можете установить его свойство **CacheSize** до 20 для отображения одновременно 20 записей.</span><span class="sxs-lookup"><span data-stu-id="a9f74-120">For example, if you're using a **Recordset** object as the source of the data to be displayed on screen, you could set its **CacheSize** property to 20 to display 20 records at one time.</span></span>

<span data-ttu-id="a9f74-121">Двигатель базы данных Microsoft Access запрашивает записи в кэше в диапазоне от кэша, а записи за пределами кэша запрашивает сервер.</span><span class="sxs-lookup"><span data-stu-id="a9f74-121">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="a9f74-122">Записи, извлеченные из кэша, не отражают одновременно внесенные другими пользователями изменения в исходные данные.</span><span class="sxs-lookup"><span data-stu-id="a9f74-122">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

<span data-ttu-id="a9f74-123">Чтобы принудить к обновлению всех кэшных данных, установите свойство **CacheSize** объекта **Recordset** до 0, повторно установите его до размера первоначально запрашиваемого кэша, а затем используйте метод **FillCache.**</span><span class="sxs-lookup"><span data-stu-id="a9f74-123">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

## <a name="example"></a><span data-ttu-id="a9f74-124">Пример</span><span class="sxs-lookup"><span data-stu-id="a9f74-124">Example</span></span>

<span data-ttu-id="a9f74-125">В этом примере используются методы **CreateTableDef** и **FillCache** и свойства **CacheSize**, **CacheStart** и **SourceTableName** для перечисления записей в связанной таблице два раза.</span><span class="sxs-lookup"><span data-stu-id="a9f74-125">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice.</span></span> <span data-ttu-id="a9f74-126">Затем выполняется перечисление дважды с кэшем в 50 записей.</span><span class="sxs-lookup"><span data-stu-id="a9f74-126">Then it enumerates the records twice with a 50-record cache.</span></span> <span data-ttu-id="a9f74-127">Затем пример отображает статистику производительности для некэшированных и кэшированных запусков в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="a9f74-127">The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset2 
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
