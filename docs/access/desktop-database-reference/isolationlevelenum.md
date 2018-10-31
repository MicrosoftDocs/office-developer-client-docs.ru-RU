---
title: IsolationLevelEnum (Справочник по для настольных баз данных Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7e32cd3c8ae78199f90fcac8cccdf377bf332d38
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863943"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="2b85d-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="2b85d-102">IsolationLevelEnum</span></span>

<span data-ttu-id="2b85d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b85d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2b85d-104">Указывает уровень изоляции транзакций для объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2b85d-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b85d-105">Константа</span><span class="sxs-lookup"><span data-stu-id="2b85d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2b85d-106">Значение</span><span class="sxs-lookup"><span data-stu-id="2b85d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2b85d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2b85d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b85d-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="2b85d-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="2b85d-109">-1</span><span class="sxs-lookup"><span data-stu-id="2b85d-109">-1</span></span></p></td>
<td><p><span data-ttu-id="2b85d-110">Указывает, что поставщик использует уровень изоляции не указан, но не удается определить уровень.</span><span class="sxs-lookup"><span data-stu-id="2b85d-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b85d-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="2b85d-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="2b85d-112">16</span><span class="sxs-lookup"><span data-stu-id="2b85d-112">16</span></span></p></td>
<td><p><span data-ttu-id="2b85d-113">Указывает, что ожидающие изменения более изолированных транзакций не могут быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="2b85d-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b85d-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="2b85d-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="2b85d-115">256</span><span class="sxs-lookup"><span data-stu-id="2b85d-115">256</span></span></p></td>
<td><p><span data-ttu-id="2b85d-116">Указывает, что из одной операции можно просмотреть несохраненные изменения в других операций.</span><span class="sxs-lookup"><span data-stu-id="2b85d-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b85d-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="2b85d-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="2b85d-118">256</span><span class="sxs-lookup"><span data-stu-id="2b85d-118">256</span></span></p></td>
<td><p><span data-ttu-id="2b85d-119">То же, что <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b85d-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b85d-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="2b85d-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="2b85d-121">4096</span><span class="sxs-lookup"><span data-stu-id="2b85d-121">4096</span></span></p></td>
<td><p><span data-ttu-id="2b85d-122">Указывает, что из одной операции можно просмотреть изменения в другие транзакции только после их фиксации.</span><span class="sxs-lookup"><span data-stu-id="2b85d-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b85d-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="2b85d-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="2b85d-124">4096</span><span class="sxs-lookup"><span data-stu-id="2b85d-124">4096</span></span></p></td>
<td><p><span data-ttu-id="2b85d-125">То же, что <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b85d-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b85d-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="2b85d-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="2b85d-127">65536</span><span class="sxs-lookup"><span data-stu-id="2b85d-127">65536</span></span></p></td>
<td><p><span data-ttu-id="2b85d-128">Указывает, что из одной операции нельзя просмотреть изменения, внесенные в других операций, но, обновление можно извлечь новые объекты <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="2b85d-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b85d-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="2b85d-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="2b85d-130">1048576</span><span class="sxs-lookup"><span data-stu-id="2b85d-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="2b85d-131">Указывает, что транзакции выполняются по отдельности других операций.</span><span class="sxs-lookup"><span data-stu-id="2b85d-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b85d-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="2b85d-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="2b85d-133">1048576</span><span class="sxs-lookup"><span data-stu-id="2b85d-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="2b85d-134">То же, что <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b85d-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2b85d-135">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2b85d-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="2b85d-136">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2b85d-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b85d-137">Constant</span><span class="sxs-lookup"><span data-stu-id="2b85d-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b85d-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="2b85d-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b85d-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="2b85d-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b85d-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="2b85d-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b85d-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="2b85d-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b85d-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="2b85d-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b85d-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="2b85d-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b85d-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="2b85d-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b85d-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="2b85d-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b85d-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="2b85d-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

