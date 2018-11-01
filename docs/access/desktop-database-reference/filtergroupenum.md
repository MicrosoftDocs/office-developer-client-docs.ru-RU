---
title: FilterGroupEnum (Справочник по для настольных баз данных Access)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5c42b703536e931405325d3a91219a148e6580d1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873289"
---
# <a name="filtergroupenum"></a><span data-ttu-id="e47c5-102">FilterGroupEnum</span><span class="sxs-lookup"><span data-stu-id="e47c5-102">FilterGroupEnum</span></span>

<span data-ttu-id="e47c5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e47c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e47c5-104">Указывает группу записей для фильтрации из [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e47c5-104">Specifies the group of records to be filtered from a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e47c5-105">Константа</span><span class="sxs-lookup"><span data-stu-id="e47c5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e47c5-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e47c5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e47c5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e47c5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e47c5-108"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="e47c5-108"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="e47c5-109">2</span><span class="sxs-lookup"><span data-stu-id="e47c5-109">2</span></span></p></td>
<td><p><span data-ttu-id="e47c5-110">Фильтры для просмотра только записей, влияет на последнем вызове <a href="delete-method-ado-recordset.md">Удаление</a>, <a href="resync-method-ado.md">выполнить повторную синхронизацию</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a>или <a href="cancelbatch-method-ado.md">CancelBatch</a> .</span><span class="sxs-lookup"><span data-stu-id="e47c5-110">Filters for viewing only records affected by the last <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a>, or <a href="cancelbatch-method-ado.md">CancelBatch</a> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e47c5-111"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="e47c5-111"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="e47c5-112">5</span><span class="sxs-lookup"><span data-stu-id="e47c5-112">5</span></span></p></td>
<td><p><span data-ttu-id="e47c5-113">Фильтры для просмотра записей, которые не удалось последнего обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="e47c5-113">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e47c5-114"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="e47c5-114"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="e47c5-115">3</span><span class="sxs-lookup"><span data-stu-id="e47c5-115">3</span></span></p></td>
<td><p><span data-ttu-id="e47c5-116">Фильтры для просмотра записей в кэше текущего — то есть, результаты последнего звонка для извлечения записей из базы данных.</span><span class="sxs-lookup"><span data-stu-id="e47c5-116">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e47c5-117"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="e47c5-117"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="e47c5-118">0</span><span class="sxs-lookup"><span data-stu-id="e47c5-118">0</span></span></p></td>
<td><p><span data-ttu-id="e47c5-119">Удаляет текущий фильтр и восстанавливает все записи для просмотра.</span><span class="sxs-lookup"><span data-stu-id="e47c5-119">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e47c5-120"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="e47c5-120"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="e47c5-121">1</span><span class="sxs-lookup"><span data-stu-id="e47c5-121">1</span></span></p></td>
<td><p><span data-ttu-id="e47c5-122">Фильтры для просмотра только записей, были изменены, но еще не были отправлены на сервер.</span><span class="sxs-lookup"><span data-stu-id="e47c5-122">Filters for viewing only records that have changed but have not yet been sent to the server.</span></span> <span data-ttu-id="e47c5-123">Применимо только к режим пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="e47c5-123">Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e47c5-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="e47c5-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="e47c5-125">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="e47c5-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e47c5-126">Constant</span><span class="sxs-lookup"><span data-stu-id="e47c5-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e47c5-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="e47c5-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e47c5-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="e47c5-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e47c5-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="e47c5-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e47c5-130">AdoEnums.FilterGroup.NONE</span><span class="sxs-lookup"><span data-stu-id="e47c5-130">AdoEnums.FilterGroup.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e47c5-131">AdoEnums.FilterGroup.PENDINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="e47c5-131">AdoEnums.FilterGroup.PENDINGRECORDS</span></span></p></td>
</tr>
</tbody>
</table>

