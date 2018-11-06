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
ms.openlocfilehash: ef0f4ad298e316cbae295bcf4f6c4c5349b18655
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998534"
---
# <a name="recordset2fillcache-method-dao"></a><span data-ttu-id="a59c7-102">Метод Recordset2.FillCache (DAO)</span><span class="sxs-lookup"><span data-stu-id="a59c7-102">Recordset2.FillCache method (DAO)</span></span>

<span data-ttu-id="a59c7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a59c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a59c7-104">Заполняет все или часть из локального кэша для объекта **набора записей** , который содержит данные из Microsoft Access базы данных подключен модуль ODBC источника данных (Microsoft Access базы данных подключен модуль ODBC только баз данных).</span><span class="sxs-lookup"><span data-stu-id="a59c7-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a59c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a59c7-105">Syntax</span></span>

<span data-ttu-id="a59c7-106">*выражение* . FillCache (***строк***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="a59c7-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="a59c7-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="a59c7-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a59c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a59c7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a59c7-109">Имя</span><span class="sxs-lookup"><span data-stu-id="a59c7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a59c7-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="a59c7-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="a59c7-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a59c7-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="a59c7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a59c7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a59c7-113"><em>Строк</em></span><span class="sxs-lookup"><span data-stu-id="a59c7-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="a59c7-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a59c7-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="a59c7-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a59c7-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a59c7-116"><strong>Variant</strong> (<strong>Integer</strong> подтип), указывающее число строк для хранения в кэше.</span><span class="sxs-lookup"><span data-stu-id="a59c7-116">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache.</span></span> <span data-ttu-id="a59c7-117">Если опустить аргумент значение определяется значение свойства <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="a59c7-117">If you omit this argument, the value is determined by the <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a59c7-118"><em>StartBookmark</em></span><span class="sxs-lookup"><span data-stu-id="a59c7-118"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="a59c7-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a59c7-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="a59c7-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a59c7-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a59c7-121"><strong>Variant</strong> (<strong>String</strong> подтип), указывающее закладку.</span><span class="sxs-lookup"><span data-stu-id="a59c7-121">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark.</span></span> <span data-ttu-id="a59c7-122">Наполнения кэша, начиная с записи, указанный в параметре эту закладку.</span><span class="sxs-lookup"><span data-stu-id="a59c7-122">The cache is filled starting from the record indicated by this bookmark.</span></span> <span data-ttu-id="a59c7-123">Если опустить аргумент наполнения кэша начиная с записи, указанный в параметре свойство <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="a59c7-123">If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a59c7-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a59c7-124">Remarks</span></span>

<span data-ttu-id="a59c7-125">Кэширование повышает производительность приложения, которое получает данные с удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="a59c7-125">Caching improves the performance of an application that retrieves data from a remote server.</span></span> <span data-ttu-id="a59c7-126">Кэш — это место в локальной памяти, в которой содержатся данные, недавно извлеченные с сервера. предполагается, что данные, вероятно, запрашивается еще раз во время выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="a59c7-126">A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running.</span></span> <span data-ttu-id="a59c7-127">Когда пользователь запрашивает данные, ядро базы данных Microsoft Access кэша для данных сначала проверяет вместо извлечение из сервера, который занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="a59c7-127">When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time.</span></span> <span data-ttu-id="a59c7-128">Кэш не сохраняет данные, которые не поступают из источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="a59c7-128">The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="a59c7-129">Без необходимости кэша следует реализовать с записями, как их загрузки, можно использовать метод **FillCache** для явно заполнения кэша в любое время.</span><span class="sxs-lookup"><span data-stu-id="a59c7-129">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time.</span></span> <span data-ttu-id="a59c7-130">Это более быстрый способ заполнения кэша, так как **FillCache** извлекает несколько записей вместо того, по одному.</span><span class="sxs-lookup"><span data-stu-id="a59c7-130">This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time.</span></span> <span data-ttu-id="a59c7-131">К примеру во время просмотра каждого один экран записей приложение использует **FillCache** для получения следующей экранной записи для просмотра.</span><span class="sxs-lookup"><span data-stu-id="a59c7-131">For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="a59c7-132">Microsoft Access базы данных engine подключенных источников данных ODBC, доступ с помощью объектов **наборов записей** может иметь локального кэша.</span><span class="sxs-lookup"><span data-stu-id="a59c7-132">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache.</span></span> <span data-ttu-id="a59c7-133">Чтобы создать кэш, откройте объект **набора записей** из к удаленному источнику данных и задайте его свойства **CacheSize** и **CacheStart** **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="a59c7-133">To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="a59c7-134">Если строк и startbookmark создать диапазон записей, частично или полностью вне диапазона записей, указанное в свойствах **CacheSize** и **CacheStart** , часть записей за пределами этого диапазона игнорируется и не удается загрузить в кэш.</span><span class="sxs-lookup"><span data-stu-id="a59c7-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="a59c7-135">Если **FillCache** запрашивает записей больше, чем номер, оставшихся в к удаленному источнику данных, ядро базы данных Microsoft Access извлекаются только оставшихся записей и ошибка не происходит.</span><span class="sxs-lookup"><span data-stu-id="a59c7-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="a59c7-136">Записей, полученных из кэша не отражает параллельных изменений других пользователей в источник данных.</span><span class="sxs-lookup"><span data-stu-id="a59c7-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>
> - <span data-ttu-id="a59c7-137">**FillCache** только извлекает записи еще не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="a59c7-137">**FillCache** only retrieves records not already cached.</span></span> <span data-ttu-id="a59c7-138">Чтобы принудительно выполнить обновление всех кэшированных данных, присвойте свойству **CacheSize** **записей** значение 0, сбросить его размер кэша, который изначально запрошен и затем с помощью **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="a59c7-138">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.</span></span>

## <a name="example"></a><span data-ttu-id="a59c7-139">Пример</span><span class="sxs-lookup"><span data-stu-id="a59c7-139">Example</span></span>

<span data-ttu-id="a59c7-140">В этом примере используется **CacheSize**, **CacheStart** и **SourceTableName** свойства и методы **CreateTableDef** и **FillCache** дважды перечисление записей в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="a59c7-140">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice.</span></span> <span data-ttu-id="a59c7-141">Затем выполняется перечисление записей дважды с 50 записи кэша.</span><span class="sxs-lookup"><span data-stu-id="a59c7-141">Then it enumerates the records twice with a 50-record cache.</span></span> <span data-ttu-id="a59c7-142">Затем отображается статистика производительности без кэш-памяти и кэшированные просматривает связанную таблицу.</span><span class="sxs-lookup"><span data-stu-id="a59c7-142">The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
