---
title: FilterGroupEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2ce54fe743c46468850abc5dc16520e208ec9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292421"
---
# <a name="filtergroupenum"></a><span data-ttu-id="bd696-102">FilterGroupEnum</span><span class="sxs-lookup"><span data-stu-id="bd696-102">FilterGroupEnum</span></span>

<span data-ttu-id="bd696-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd696-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd696-104">Указывает группу записей, которые необходимо отфильтровать из [наборов записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="bd696-104">Specifies the group of records to be filtered from a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd696-105">Константа</span><span class="sxs-lookup"><span data-stu-id="bd696-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="bd696-106">Значение</span><span class="sxs-lookup"><span data-stu-id="bd696-106">Value</span></span></p></th>
<th><p><span data-ttu-id="bd696-107">Описание</span><span class="sxs-lookup"><span data-stu-id="bd696-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd696-108"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="bd696-108"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="bd696-109">2 </span><span class="sxs-lookup"><span data-stu-id="bd696-109">2</span></span></p></td>
<td><p><span data-ttu-id="bd696-110">Фильтры для просмотра только записей, затронутых последним вызовом <a href="delete-method-ado-recordset.md">Delete,</a> <a href="resync-method-ado.md">Resync,</a> <a href="updatebatch-method-ado.md">UpdateBatch</a>или <a href="cancelbatch-method-ado.md">CancelBatch.</a></span><span class="sxs-lookup"><span data-stu-id="bd696-110">Filters for viewing only records affected by the last <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a>, or <a href="cancelbatch-method-ado.md">CancelBatch</a> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd696-111"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="bd696-111"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="bd696-112">5 </span><span class="sxs-lookup"><span data-stu-id="bd696-112">5</span></span></p></td>
<td><p><span data-ttu-id="bd696-113">Фильтры для просмотра записей, которые не удалось обновить последним пакетным обновлением.</span><span class="sxs-lookup"><span data-stu-id="bd696-113">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd696-114"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="bd696-114"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="bd696-115">3 </span><span class="sxs-lookup"><span data-stu-id="bd696-115">3</span></span></p></td>
<td><p><span data-ttu-id="bd696-116">Фильтры для просмотра записей в текущем кэше, то есть результатов последнего вызова для получения записей из базы данных.</span><span class="sxs-lookup"><span data-stu-id="bd696-116">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd696-117"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="bd696-117"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="bd696-118">0</span><span class="sxs-lookup"><span data-stu-id="bd696-118">0</span></span></p></td>
<td><p><span data-ttu-id="bd696-119">Удаляет текущий фильтр и восстанавливает все записи для просмотра.</span><span class="sxs-lookup"><span data-stu-id="bd696-119">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd696-120"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="bd696-120"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="bd696-121">1 </span><span class="sxs-lookup"><span data-stu-id="bd696-121">1</span></span></p></td>
<td><p><span data-ttu-id="bd696-122">Фильтры для просмотра только тех записей, которые были изменены, но еще не отправлены на сервер.</span><span class="sxs-lookup"><span data-stu-id="bd696-122">Filters for viewing only records that have changed but have not yet been sent to the server.</span></span> <span data-ttu-id="bd696-123">Применимо только для режима пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="bd696-123">Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="bd696-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="bd696-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="bd696-125">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="bd696-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd696-126">Константа</span><span class="sxs-lookup"><span data-stu-id="bd696-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd696-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="bd696-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd696-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="bd696-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd696-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="bd696-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd696-130">AdoEnums.FilterGroup.NONE</span><span class="sxs-lookup"><span data-stu-id="bd696-130">AdoEnums.FilterGroup.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd696-131">AdoEnums.FilterGroup.PENDINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="bd696-131">AdoEnums.FilterGroup.PENDINGRECORDS</span></span></p></td>
</tr>
</tbody>
</table>

