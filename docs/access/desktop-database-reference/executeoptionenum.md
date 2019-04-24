---
title: Ексекутеоптионенум (Справочник по базам данных Access на компьютере)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: febeb3b52eb579647c995b01d6723a5c1f1b0c1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293247"
---
# <a name="executeoptionenum"></a><span data-ttu-id="d6598-102">ExecuteOptionEnum</span><span class="sxs-lookup"><span data-stu-id="d6598-102">ExecuteOptionEnum</span></span>

<span data-ttu-id="d6598-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6598-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6598-104">Указывает, как поставщик должен выполнять команду.</span><span class="sxs-lookup"><span data-stu-id="d6598-104">Specifies how a provider should execute a command.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6598-105">Константа</span><span class="sxs-lookup"><span data-stu-id="d6598-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d6598-106">Значение</span><span class="sxs-lookup"><span data-stu-id="d6598-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d6598-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d6598-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6598-108"><strong>Адасинцексекуте</strong></span><span class="sxs-lookup"><span data-stu-id="d6598-108"><strong>adAsyncExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="d6598-109">0x10</span><span class="sxs-lookup"><span data-stu-id="d6598-109">0x10</span></span></p></td>
<td><p><span data-ttu-id="d6598-110">Указывает, что команда должна выполняться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d6598-110">Indicates that the command should execute asynchronously.</span></span> <span data-ttu-id="d6598-111">Это значение не может сочетаться со <a href="commandtypeenum.md"></a> значением коммандтипинум <strong>адкмдтабледирект</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6598-111">This value cannot be combined with the <a href="commandtypeenum.md">CommandTypeEnum</a> value <strong>adCmdTableDirect</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6598-112"><strong>Адасинкфетч</strong></span><span class="sxs-lookup"><span data-stu-id="d6598-112"><strong>adAsyncFetch</strong></span></span></p></td>
<td><p><span data-ttu-id="d6598-113">0x20</span><span class="sxs-lookup"><span data-stu-id="d6598-113">0x20</span></span></p></td>
<td><p><span data-ttu-id="d6598-114">Указывает, что оставшиеся строки после начального количества, указанного в свойстве <a href="cachesize-property-ado.md">CacheSize</a> , должны быть получены асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d6598-114">Indicates that the remaining rows after the initial quantity specified in the <a href="cachesize-property-ado.md">CacheSize</a> property should be retrieved asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6598-115"><strong>Адасинкфетчнонблоккинг</strong></span><span class="sxs-lookup"><span data-stu-id="d6598-115"><strong>adAsyncFetchNonBlocking</strong></span></span></p></td>
<td><p><span data-ttu-id="d6598-116">0x40</span><span class="sxs-lookup"><span data-stu-id="d6598-116">0x40</span></span></p></td>
<td><p><span data-ttu-id="d6598-117">Указывает, что главный поток никогда не блокируется при извлечении.</span><span class="sxs-lookup"><span data-stu-id="d6598-117">Indicates that the main thread never blocks while retrieving.</span></span> <span data-ttu-id="d6598-118">Если запрашиваемая строка не была получена, текущая строка автоматически перемещается в конец файла.</span><span class="sxs-lookup"><span data-stu-id="d6598-118">If the requested row has not been retrieved, the current row automatically moves to the end of the file.</span></span></p><p><span data-ttu-id="d6598-119">Если вы откроете <a href="recordset-object-ado.md">набор записей</a> из <a href="stream-object-ado.md">потока</a> , содержащего сохраняемый <strong>набор записей</strong>, <strong>адасинкфетчнонблоккинг</strong> не будет оказывать никакого результата; операция будет синхронной и блокирующей.</span><span class="sxs-lookup"><span data-stu-id="d6598-119">If you open a <a href="recordset-object-ado.md">Recordset</a> from a <a href="stream-object-ado.md">Stream</a> containing a persistently stored <strong>Recordset</strong>, <strong>adAsyncFetchNonBlocking</strong> will not have an effect; the operation will be synchronous and blocking.</span></span> <span data-ttu-id="d6598-120"><strong>адасинчфетчнонблоккинг</strong> не оказывает никакого действия, если для открытия объекта <strong>Recordset</strong>используется параметр <a href="commandtypeenum.md">адкмдтабледирект</a> .</span><span class="sxs-lookup"><span data-stu-id="d6598-120"><strong>adAsynchFetchNonBlocking</strong> has no effect when the <a href="commandtypeenum.md">adCmdTableDirect</a> option is used to open the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6598-121"><strong>Адексекутенорекордс</strong></span><span class="sxs-lookup"><span data-stu-id="d6598-121"><strong>adExecuteNoRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="d6598-122">0x80</span><span class="sxs-lookup"><span data-stu-id="d6598-122">0x80</span></span></p></td>
<td><p><span data-ttu-id="d6598-123">Указывает, что текст команды — это команда или хранимая процедура, не возвращающая строки (например, команда, которая вставляет только данные).</span><span class="sxs-lookup"><span data-stu-id="d6598-123">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</span></span> <span data-ttu-id="d6598-124">Если извлекаются какие бы то ни было строки, они отбрасываются и не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="d6598-124">If any rows are retrieved, they are discarded and not returned.</span></span> <span data-ttu-id="d6598-125"><strong>адексекутенорекордс</strong> можно передать только как необязательный параметр для метода <strong></strong> или метода <strong>подключения</strong> <strong>EXECUTE</strong> .</span><span class="sxs-lookup"><span data-stu-id="d6598-125"><strong>adExecuteNoRecords</strong> can only be passed as an optional parameter to the <strong>Command</strong> or <strong>Connection</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6598-126"><strong>Адексекутестреам</strong></span><span class="sxs-lookup"><span data-stu-id="d6598-126"><strong>adExecuteStream</strong></span></span></p></td>
<td><p><span data-ttu-id="d6598-127">0x400</span><span class="sxs-lookup"><span data-stu-id="d6598-127">0x400</span></span></p></td>
<td><p><span data-ttu-id="d6598-128">Указывает, что результаты выполнения команды должны возвращаться в виде потока.</span><span class="sxs-lookup"><span data-stu-id="d6598-128">Indicates that the results of a command execution should be returned as a stream.</span></span> <span data-ttu-id="d6598-129"><strong>адексекутестреам</strong> можно передавать в качестве необязательного параметра методу <strong></strong> <strong>EXECUTE</strong> Command.</span><span class="sxs-lookup"><span data-stu-id="d6598-129"><strong>adExecuteStream</strong> can only be passed as an optional parameter to the <strong>Command</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6598-130"><strong>Адексекутерекорд</strong></span><span class="sxs-lookup"><span data-stu-id="d6598-130"><strong>adExecuteRecord</strong></span></span></p></td>
<td><p><br />
</p></td>
<td><p><span data-ttu-id="d6598-131">Указывает, что <strong>CommandText</strong> — это команда или хранимая процедура, возвращающая одну строку, которая должна возвращаться как объект <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="d6598-131">Indicates that the <strong>CommandText</strong> is a command or stored procedure that returns a single row which should be returned as a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6598-132"><strong>АдоптионунспеЦифиед</strong></span><span class="sxs-lookup"><span data-stu-id="d6598-132"><strong>adOptionUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="d6598-133">–1</span><span class="sxs-lookup"><span data-stu-id="d6598-133">-1</span></span></p></td>
<td><p><span data-ttu-id="d6598-134">Указывает, что команда не задана.</span><span class="sxs-lookup"><span data-stu-id="d6598-134">Indicates that the command is unspecified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d6598-135">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d6598-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="d6598-136">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="d6598-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6598-137">Константа</span><span class="sxs-lookup"><span data-stu-id="d6598-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6598-138">Адоенумс. Ексекутеоптион. АСИНЦЕКСЕКУТЕ</span><span class="sxs-lookup"><span data-stu-id="d6598-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6598-139">Адоенумс. Ексекутеоптион. АСИНКФЕТЧ</span><span class="sxs-lookup"><span data-stu-id="d6598-139">AdoEnums.ExecuteOption.ASYNCFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6598-140">Адоенумс. Ексекутеоптион. АСИНКФЕТЧНОНБЛОККИНГ</span><span class="sxs-lookup"><span data-stu-id="d6598-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6598-141">Адоенумс. Ексекутеоптион. unRECORDs</span><span class="sxs-lookup"><span data-stu-id="d6598-141">AdoEnums.ExecuteOption.NORECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6598-142">Адоенумс. Ексекутеоптион. unspecifieded</span><span class="sxs-lookup"><span data-stu-id="d6598-142">AdoEnums.ExecuteOption.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

