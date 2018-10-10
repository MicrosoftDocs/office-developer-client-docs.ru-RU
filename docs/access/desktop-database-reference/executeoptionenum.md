---
title: ExecuteOptionEnum (Справочник по для настольных баз данных Access)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aeb1083c693e0848e30a0b9217ae709994daddb5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481308"
---
# <a name="executeoptionenum"></a><span data-ttu-id="303bc-102">ExecuteOptionEnum</span><span class="sxs-lookup"><span data-stu-id="303bc-102">ExecuteOptionEnum</span></span>


<span data-ttu-id="303bc-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="303bc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="303bc-104">Указывает, как поставщик должен выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="303bc-104">Specifies how a provider should execute a command.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="303bc-105">Константа</span><span class="sxs-lookup"><span data-stu-id="303bc-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="303bc-106">Значение</span><span class="sxs-lookup"><span data-stu-id="303bc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="303bc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="303bc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="303bc-108"><strong>adAsyncExecute</strong></span><span class="sxs-lookup"><span data-stu-id="303bc-108"><strong>adAsyncExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="303bc-109">0x10</span><span class="sxs-lookup"><span data-stu-id="303bc-109">0x10</span></span></p></td>
<td><p><span data-ttu-id="303bc-110">Указывает, что будет выполняться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="303bc-110">Indicates that the command should execute asynchronously.</span></span> <span data-ttu-id="303bc-111">Это значение не может быть вместе с значение <a href="commandtypeenum.md">CommandTypeEnum</a> <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="303bc-111">This value cannot be combined with the <a href="commandtypeenum.md">CommandTypeEnum</a> value <strong>adCmdTableDirect</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="303bc-112"><strong>adAsyncFetch</strong></span><span class="sxs-lookup"><span data-stu-id="303bc-112"><strong>adAsyncFetch</strong></span></span></p></td>
<td><p><span data-ttu-id="303bc-113">0x20</span><span class="sxs-lookup"><span data-stu-id="303bc-113">0x20</span></span></p></td>
<td><p><span data-ttu-id="303bc-114">Указывает, что оставшиеся строки после начального количества, указанных в свойстве <a href="cachesize-property-ado.md">CacheSize</a> должны быть получены асинхронно.</span><span class="sxs-lookup"><span data-stu-id="303bc-114">Indicates that the remaining rows after the initial quantity specified in the <a href="cachesize-property-ado.md">CacheSize</a> property should be retrieved asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="303bc-115"><strong>adAsyncFetchNonBlocking</strong></span><span class="sxs-lookup"><span data-stu-id="303bc-115"><strong>adAsyncFetchNonBlocking</strong></span></span></p></td>
<td><p><span data-ttu-id="303bc-116">0x40</span><span class="sxs-lookup"><span data-stu-id="303bc-116">0x40</span></span></p></td>
<td><p><span data-ttu-id="303bc-117">Указывает, что основной поток не блокируется при получении.</span><span class="sxs-lookup"><span data-stu-id="303bc-117">Indicates that the main thread never blocks while retrieving.</span></span> <span data-ttu-id="303bc-118">Если не был получен запрашиваемый строку, текущей строки автоматически перемещается в конец файла.</span><span class="sxs-lookup"><span data-stu-id="303bc-118">If the requested row has not been retrieved, the current row automatically moves to the end of the file.</span></span> <span data-ttu-id="303bc-119">При открытии <a href="recordset-object-ado.md">набора записей</a> из <a href="stream-object-ado.md">потока</a> , содержащий постоянно сохраненных <strong>записей</strong> <strong>adAsyncFetchNonBlocking</strong> не будет иметь эффекта. Операция будет синхронная и блокировки.</span><span class="sxs-lookup"><span data-stu-id="303bc-119">If you open a <a href="recordset-object-ado.md">Recordset</a> from a <a href="stream-object-ado.md">Stream</a> containing a persistently stored <strong>Recordset</strong>, <strong>adAsyncFetchNonBlocking</strong> will not have an effect; the operation will be synchronous and blocking.</span></span> <span data-ttu-id="303bc-120"><strong>adAsynchFetchNonBlocking</strong> не оказывает влияния при использовании параметра <a href="commandtypeenum.md">adCmdTableDirect</a> для открытия <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="303bc-120"><strong>adAsynchFetchNonBlocking</strong> has no effect when the <a href="commandtypeenum.md">adCmdTableDirect</a> option is used to open the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="303bc-121"><strong>adExecuteNoRecords</strong></span><span class="sxs-lookup"><span data-stu-id="303bc-121"><strong>adExecuteNoRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="303bc-122">0x80</span><span class="sxs-lookup"><span data-stu-id="303bc-122">0x80</span></span></p></td>
<td><p><span data-ttu-id="303bc-123">Указывает, что текст команды команду или хранимую процедуру, которая не возвращает строки (например, команды, только вставляет данные).</span><span class="sxs-lookup"><span data-stu-id="303bc-123">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</span></span> <span data-ttu-id="303bc-124">Если извлекаются все строки, они удалены и не возвращается.</span><span class="sxs-lookup"><span data-stu-id="303bc-124">If any rows are retrieved, they are discarded and not returned.</span></span> <span data-ttu-id="303bc-125"><strong>adExecuteNoRecords</strong> можно только передаваться как необязательный параметр <strong>команда</strong> или метод <strong>Execute</strong> <strong>подключения</strong> .</span><span class="sxs-lookup"><span data-stu-id="303bc-125"><strong>adExecuteNoRecords</strong> can only be passed as an optional parameter to the <strong>Command</strong> or <strong>Connection</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="303bc-126"><strong>adExecuteStream</strong></span><span class="sxs-lookup"><span data-stu-id="303bc-126"><strong>adExecuteStream</strong></span></span></p></td>
<td><p><span data-ttu-id="303bc-127">0x400</span><span class="sxs-lookup"><span data-stu-id="303bc-127">0x400</span></span></p></td>
<td><p><span data-ttu-id="303bc-128">Указывает, что результаты выполнения команды должны возвращаться в виде потока.</span><span class="sxs-lookup"><span data-stu-id="303bc-128">Indicates that the results of a command execution should be returned as a stream.</span></span> <span data-ttu-id="303bc-129"><strong>adExecuteStream</strong> могут передаваться только как необязательный параметр для метода <strong>Execute</strong> <strong>команды</strong> .</span><span class="sxs-lookup"><span data-stu-id="303bc-129"><strong>adExecuteStream</strong> can only be passed as an optional parameter to the <strong>Command</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="303bc-130"><strong>adExecuteRecord</strong></span><span class="sxs-lookup"><span data-stu-id="303bc-130"><strong>adExecuteRecord</strong></span></span></p></td>
<td><p><br />
</p></td>
<td><p><span data-ttu-id="303bc-131">Указывает, что <strong>CommandText</strong> команду или хранимую процедуру, возвращающую одной строки, которые должны быть возвращены как объект <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="303bc-131">Indicates that the <strong>CommandText</strong> is a command or stored procedure that returns a single row which should be returned as a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="303bc-132"><strong>adOptionUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="303bc-132"><strong>adOptionUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="303bc-133">-1</span><span class="sxs-lookup"><span data-stu-id="303bc-133">-1</span></span></p></td>
<td><p><span data-ttu-id="303bc-134">Указывает, что команда не определено.</span><span class="sxs-lookup"><span data-stu-id="303bc-134">Indicates that the command is unspecified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="303bc-135">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="303bc-135">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="303bc-136">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="303bc-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="303bc-137">Constant</span><span class="sxs-lookup"><span data-stu-id="303bc-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="303bc-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span><span class="sxs-lookup"><span data-stu-id="303bc-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="303bc-139">AdoEnums.ExecuteOption.ASYNCFETCH</span><span class="sxs-lookup"><span data-stu-id="303bc-139">AdoEnums.ExecuteOption.ASYNCFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="303bc-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span><span class="sxs-lookup"><span data-stu-id="303bc-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="303bc-141">AdoEnums.ExecuteOption.NORECORDS</span><span class="sxs-lookup"><span data-stu-id="303bc-141">AdoEnums.ExecuteOption.NORECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="303bc-142">AdoEnums.ExecuteOption.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="303bc-142">AdoEnums.ExecuteOption.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

