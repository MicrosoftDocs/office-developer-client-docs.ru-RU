---
title: Метод Recordset2.FillCache (DAO)
TOCTitle: FillCache Method
ms:assetid: 28a70997-a8d4-73e6-171a-61286e3d3485
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192007(v=office.15)
ms:contentKeyID: 48543864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052942
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2098df82375ac47b7d5abe0bd63b0af2bb29ba40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309704"
---
# <a name="recordset2fillcache-method-dao"></a><span data-ttu-id="decb1-102">Метод Recordset2.FillCache (DAO)</span><span class="sxs-lookup"><span data-stu-id="decb1-102">Recordset2.FillCache method (DAO)</span></span>

<span data-ttu-id="decb1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="decb1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="decb1-104">Заполняет полностью или частично локальный кэш для объекта **Recordset**, который содержит данные из источника ODBC, подключенного к ядру СУБД Microsoft Access (только для баз данных ODBC, подключенных к Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="decb1-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="decb1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="decb1-105">Syntax</span></span>

<span data-ttu-id="decb1-106">*выражение .* FillCache(***Rows***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="decb1-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="decb1-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="decb1-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="decb1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="decb1-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="decb1-109">Имя</span><span class="sxs-lookup"><span data-stu-id="decb1-109">Name</span></span></p></th>
<th><p><span data-ttu-id="decb1-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="decb1-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="decb1-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="decb1-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="decb1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="decb1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="decb1-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="decb1-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="decb1-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="decb1-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="decb1-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="decb1-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="decb1-116">Вариант <strong></strong> <strong>(подтип integer),</strong> который указывает количество строк для хранения в кэше.</span><span class="sxs-lookup"><span data-stu-id="decb1-116">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache.</span></span> <span data-ttu-id="decb1-117">Если не упустить этот аргумент, значение определяется параметром свойства <strong><a href="recordset2-cachesize-property-dao.md">CacheSize.</a></strong></span><span class="sxs-lookup"><span data-stu-id="decb1-117">If you omit this argument, the value is determined by the <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="decb1-118"><em>StartBookmark</em></span><span class="sxs-lookup"><span data-stu-id="decb1-118"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="decb1-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="decb1-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="decb1-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="decb1-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="decb1-121">Вариант <strong></strong> <strong>(подтип строки),</strong> который указывает закладку.</span><span class="sxs-lookup"><span data-stu-id="decb1-121">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark.</span></span> <span data-ttu-id="decb1-122">Кэш заполняется начиная с записи, заданной этой закладкой.</span><span class="sxs-lookup"><span data-stu-id="decb1-122">The cache is filled starting from the record indicated by this bookmark.</span></span> <span data-ttu-id="decb1-123">Если этот аргумент не указан, кэш заполняется, начиная с записи, заданной свойством <strong><a href="recordset2-cachestart-property-dao.md">CacheStart.</a></strong></span><span class="sxs-lookup"><span data-stu-id="decb1-123">If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="decb1-124">Заметки</span><span class="sxs-lookup"><span data-stu-id="decb1-124">Remarks</span></span>

<span data-ttu-id="decb1-125">Кэшинг повышает производительность приложения, которое извлекает данные с удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="decb1-125">Caching improves the performance of an application that retrieves data from a remote server.</span></span> <span data-ttu-id="decb1-126">Кэш — это пространство в локальной памяти, в которое вмещаются данные, полученные с сервера; Предполагается, что данные, скорее всего, будут запрашиваться повторно во время работы приложения.</span><span class="sxs-lookup"><span data-stu-id="decb1-126">A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running.</span></span> <span data-ttu-id="decb1-127">Когда пользователь запрашивает данные, ячеек базы данных Microsoft Access сначала проверяет кэш на наличие данных, а не получает их с сервера, что занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="decb1-127">When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time.</span></span> <span data-ttu-id="decb1-128">Кэш не сохраняет данные, не полученные из источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="decb1-128">The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="decb1-129">Вместо того чтобы ждать заполнения кэша записями по мере их получения, можно использовать метод **FillCache** для явного заполнения кэша в любое время.</span><span class="sxs-lookup"><span data-stu-id="decb1-129">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time.</span></span> <span data-ttu-id="decb1-130">Это более быстрый способ заполнения кэша, так как **FillCache** извлекает несколько записей одновременно, а не по одной за раз.</span><span class="sxs-lookup"><span data-stu-id="decb1-130">This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time.</span></span> <span data-ttu-id="decb1-131">Например, при просмотре каждой экранной записи приложение использует **FillCache** для получения следующего экранного экрана записей для просмотра.</span><span class="sxs-lookup"><span data-stu-id="decb1-131">For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="decb1-132">Любой источник данных ODBC, подключенный к ядру базы данных Microsoft Access, к нему можно получить доступ с помощью объектов **Recordset,** может иметь локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="decb1-132">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache.</span></span> <span data-ttu-id="decb1-133">Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, а затем установите свойства **CacheSize** и **CacheStart** набора **записей.**</span><span class="sxs-lookup"><span data-stu-id="decb1-133">To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="decb1-134">Если строки и startbookmark создают диапазон записей, который частично или полностью находится за пределами диапазона записей, указанных свойствами **CacheSize** и **CacheStart,** часть объекта recordset вне этого диапазона игнорируется и не загружается в кэш.</span><span class="sxs-lookup"><span data-stu-id="decb1-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="decb1-135">Если **FillCache** запрашивает больше записей, чем число, оставшееся в удаленном источнике данных, ячее базы данных Microsoft Access извлекает только оставшиеся записи, и ошибки не возникают.</span><span class="sxs-lookup"><span data-stu-id="decb1-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="decb1-136">Записи, полученные из кэша, не отражают одновременно внесенные другими пользователями изменения в исходные данные.</span><span class="sxs-lookup"><span data-stu-id="decb1-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>
> - <span data-ttu-id="decb1-137">**FillCache** извлекает только записи, которые еще не кэшировали.</span><span class="sxs-lookup"><span data-stu-id="decb1-137">**FillCache** only retrieves records not already cached.</span></span> <span data-ttu-id="decb1-138">Чтобы принудительно обновить все кэшные данные, установите для свойства  **CacheSize** набора записей 0, сбросите его до размера кэша, который вы изначально запросили, а затем используйте **FillCache.**</span><span class="sxs-lookup"><span data-stu-id="decb1-138">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.</span></span>

## <a name="example"></a><span data-ttu-id="decb1-139">Пример</span><span class="sxs-lookup"><span data-stu-id="decb1-139">Example</span></span>

<span data-ttu-id="decb1-140">В этом примере используются методы **CreateTableDef** и **FillCache** и свойства **CacheSize**, **CacheStart** и **SourceTableName** для перечисления записей в связанной таблице два раза.</span><span class="sxs-lookup"><span data-stu-id="decb1-140">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice.</span></span> <span data-ttu-id="decb1-141">Затем выполняется перечисление дважды с кэшем в 50 записей.</span><span class="sxs-lookup"><span data-stu-id="decb1-141">Then it enumerates the records twice with a 50-record cache.</span></span> <span data-ttu-id="decb1-142">Затем пример отображает статистику производительности для некэшированных и кэшированных запусков в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="decb1-142">The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
