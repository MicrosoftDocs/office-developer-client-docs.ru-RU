---
title: Метод Recordset.FillCache (DAO)
TOCTitle: FillCache Method
ms:assetid: d171b939-b904-c6bd-6217-68bc2814e282
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834751(v=office.15)
ms:contentKeyID: 48547861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ef268a821d65732e0a54776872387f62c67e999
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300520"
---
# <a name="recordsetfillcache-method-dao"></a><span data-ttu-id="c00d3-102">Метод Recordset.FillCache (DAO)</span><span class="sxs-lookup"><span data-stu-id="c00d3-102">Recordset.FillCache method (DAO)</span></span>

<span data-ttu-id="c00d3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c00d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c00d3-104">Заполняет полностью или частично локальный кэш для объекта **Recordset**, который содержит данные из источника ODBC, подключенного к ядру СУБД Microsoft Access (только для баз данных ODBC, подключенных к Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c00d3-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c00d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c00d3-105">Syntax</span></span>

<span data-ttu-id="c00d3-106">*Expression* . FillCache (***строки***, ***стартбукмарк***)</span><span class="sxs-lookup"><span data-stu-id="c00d3-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="c00d3-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c00d3-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c00d3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c00d3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c00d3-109">Имя</span><span class="sxs-lookup"><span data-stu-id="c00d3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c00d3-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="c00d3-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="c00d3-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c00d3-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="c00d3-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c00d3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c00d3-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="c00d3-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="c00d3-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c00d3-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="c00d3-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c00d3-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c00d3-116"><strong>Variant</strong> (подтип<strong>целого числа</strong> ), который указывает количество строк для хранения в кэше.</span><span class="sxs-lookup"><span data-stu-id="c00d3-116">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache.</span></span> <span data-ttu-id="c00d3-117">Если опустить этот аргумент, значение определяется значением свойства <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="c00d3-117">If you omit this argument, the value is determined by the <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c00d3-118"><em>StartBookmark</em></span><span class="sxs-lookup"><span data-stu-id="c00d3-118"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="c00d3-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c00d3-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="c00d3-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c00d3-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c00d3-121"><strong>Variant</strong> (подтип<strong>String</strong> ), задающий закладку.</span><span class="sxs-lookup"><span data-stu-id="c00d3-121">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark.</span></span> <span data-ttu-id="c00d3-122">Заполнение кэша начинается с записи, указанной этой закладкой.</span><span class="sxs-lookup"><span data-stu-id="c00d3-122">The cache is filled starting from the record indicated by this bookmark.</span></span> <span data-ttu-id="c00d3-123">Если опустить этот аргумент, выполняется заполнение кэша, начиная с записи, указанной свойством <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="c00d3-123">If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c00d3-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="c00d3-124">Remarks</span></span>

<span data-ttu-id="c00d3-125">Кэширование повышает производительность приложения, которое получает данные с удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="c00d3-125">Caching improves the performance of an application that retrieves data from a remote server.</span></span> <span data-ttu-id="c00d3-126">Кэш — это пространство в локальной памяти, в котором хранятся данные, которые были получены последними с сервера; Предполагается, что данные, скорее всего, будут повторно запрошены во время выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="c00d3-126">A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running.</span></span> <span data-ttu-id="c00d3-127">Когда пользователь запрашивает данные, ядро СУБД Microsoft Access сначала проверяет кэш данных, а не извлекает его с сервера, что занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="c00d3-127">When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time.</span></span> <span data-ttu-id="c00d3-128">Кэш не сохраняет данные, которые не поступают из источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="c00d3-128">The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="c00d3-129">Вместо того чтобы ожидать заполнения кэша записями, можно использовать метод **FillCache** , чтобы явным образом заполнить кэш в любой момент.</span><span class="sxs-lookup"><span data-stu-id="c00d3-129">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time.</span></span> <span data-ttu-id="c00d3-130">Это более быстрый способ заполнения кэша, так как **FillCache** получает сразу несколько записей, а не по одному.</span><span class="sxs-lookup"><span data-stu-id="c00d3-130">This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time.</span></span> <span data-ttu-id="c00d3-131">Например, когда вы просматриваете каждую запись с экрана, приложение использует **FillCache** для получения следующего экрана записей для просмотра.</span><span class="sxs-lookup"><span data-stu-id="c00d3-131">For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="c00d3-132">Любой источник данных ODBC, подключенный к ядру СУБД Microsoft Access, доступ к которому осуществляется с помощью объектов **Recordset** , может иметь локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="c00d3-132">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache.</span></span> <span data-ttu-id="c00d3-133">Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, а затем задайте свойства **CacheSize** и **CacheStart** для объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c00d3-133">To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="c00d3-134">Если строки и стартбукмарк создают диапазон записей, частично или полностью вне диапазона записей, указанных в свойствах **CacheSize** и **CacheStart** , часть набора записей за пределами этого диапазона игнорируется и не будет загружаться в кэш.</span><span class="sxs-lookup"><span data-stu-id="c00d3-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="c00d3-135">Если **FillCache** запрашивает больше записей, чем число, оставшееся в удаленном источнике данных, ядро СУБД Microsoft Access извлекает только оставшиеся записи, и ошибка не возникнет.</span><span class="sxs-lookup"><span data-stu-id="c00d3-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="c00d3-136">Записи, извлеченные из кэша, не отражают параллельные изменения, внесенные другими пользователями в исходные данные.</span><span class="sxs-lookup"><span data-stu-id="c00d3-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>
> - <span data-ttu-id="c00d3-137">**FillCache** извлекает только те записи, которые еще не были кэшированы.</span><span class="sxs-lookup"><span data-stu-id="c00d3-137">**FillCache** only retrieves records not already cached.</span></span> <span data-ttu-id="c00d3-138">Чтобы принудительно обновить все кэшированные данные, присвойте свойству **CacheSize** объекта **Recordset** значение 0, сбросьте его до размера кэша, который вы изначально запросили, а затем используйте **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="c00d3-138">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.</span></span>

## <a name="example"></a><span data-ttu-id="c00d3-139">Пример</span><span class="sxs-lookup"><span data-stu-id="c00d3-139">Example</span></span>

<span data-ttu-id="c00d3-140">В этом примере используются методы **CreateTableDef** и **FillCache** и свойства **CacheSize**, **CacheStart** и **SourceTableName** для перечисления записей в связанной таблице два раза.</span><span class="sxs-lookup"><span data-stu-id="c00d3-140">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice.</span></span> <span data-ttu-id="c00d3-141">Затем выполняется перечисление дважды с кэшем в 50 записей.</span><span class="sxs-lookup"><span data-stu-id="c00d3-141">Then it enumerates the records twice with a 50-record cache.</span></span> <span data-ttu-id="c00d3-142">Затем пример отображает статистику производительности для некэшированных и кэшированных запусков в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="c00d3-142">The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
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
             "  No cache: " & Format(sngNoCache, _ 
             "##0.000") & " seconds" & vbCr & _ 
             "  50-record cache: " & Format(sngCache, _ 
             "##0.000") & " seconds" 
          .Close 
       End With 
     
       ' Delete linked table because this is a demonstration. 
       dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
       dbsCurrent.Close 
     
    End Sub
```
