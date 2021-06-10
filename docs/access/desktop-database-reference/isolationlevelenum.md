---
title: IsolationLevelEnum (Ссылка на настольные базы данных)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0176772b366b39d368f8bae1e402d420f0136c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291158"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="5f294-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="5f294-102">IsolationLevelEnum</span></span>

<span data-ttu-id="5f294-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f294-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5f294-104">Указывает уровень изоляции транзакций для объекта [Подключения.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="5f294-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f294-105">Константа</span><span class="sxs-lookup"><span data-stu-id="5f294-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="5f294-106">Значение</span><span class="sxs-lookup"><span data-stu-id="5f294-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5f294-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5f294-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f294-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="5f294-109">–1</span><span class="sxs-lookup"><span data-stu-id="5f294-109">-1</span></span></p></td>
<td><p><span data-ttu-id="5f294-110">Указывает, что поставщик использует другой уровень изоляции, чем указанный, но что уровень не может быть определен.</span><span class="sxs-lookup"><span data-stu-id="5f294-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f294-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="5f294-112">16 </span><span class="sxs-lookup"><span data-stu-id="5f294-112">16</span></span></p></td>
<td><p><span data-ttu-id="5f294-113">Указывает, что ожидающих изменений от более изолированных транзакций нельзя перезаписывать.</span><span class="sxs-lookup"><span data-stu-id="5f294-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f294-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="5f294-115">256</span><span class="sxs-lookup"><span data-stu-id="5f294-115">256</span></span></p></td>
<td><p><span data-ttu-id="5f294-116">Указывает на то, что из одной транзакции можно просматривать незаверяемые изменения в других транзакциях.</span><span class="sxs-lookup"><span data-stu-id="5f294-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f294-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="5f294-118">256</span><span class="sxs-lookup"><span data-stu-id="5f294-118">256</span></span></p></td>
<td><p><span data-ttu-id="5f294-119">То же, <strong>что и adXactBrowse.</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f294-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="5f294-121">4096</span><span class="sxs-lookup"><span data-stu-id="5f294-121">4096</span></span></p></td>
<td><p><span data-ttu-id="5f294-122">Указывает, что из одной транзакции можно просматривать изменения в других транзакциях только после их совершения.</span><span class="sxs-lookup"><span data-stu-id="5f294-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f294-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="5f294-124">4096</span><span class="sxs-lookup"><span data-stu-id="5f294-124">4096</span></span></p></td>
<td><p><span data-ttu-id="5f294-125">То <strong>же, что и adXactCursorStability.</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f294-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="5f294-127">65536</span><span class="sxs-lookup"><span data-stu-id="5f294-127">65536</span></span></p></td>
<td><p><span data-ttu-id="5f294-128">Указывает, что в одной транзакции нельзя увидеть изменения, внесенные в другие транзакции, но при этом повторное извлечение может получить <strong>новые объекты Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f294-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="5f294-130">1048576</span><span class="sxs-lookup"><span data-stu-id="5f294-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="5f294-131">Указывает, что транзакции проводятся в изоляции от других транзакций.</span><span class="sxs-lookup"><span data-stu-id="5f294-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f294-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="5f294-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="5f294-133">1048576</span><span class="sxs-lookup"><span data-stu-id="5f294-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="5f294-134">То же, <strong>что и adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="5f294-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="5f294-135">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="5f294-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="5f294-136">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="5f294-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f294-137">Константа</span><span class="sxs-lookup"><span data-stu-id="5f294-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f294-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="5f294-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f294-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="5f294-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f294-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="5f294-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f294-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="5f294-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f294-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="5f294-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f294-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="5f294-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f294-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="5f294-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f294-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="5f294-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f294-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="5f294-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

