---
title: Исолатионлевеленум (Справочник по базам данных Access на компьютере)
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
# <a name="isolationlevelenum"></a><span data-ttu-id="7f721-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="7f721-102">IsolationLevelEnum</span></span>

<span data-ttu-id="7f721-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f721-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f721-104">Задает уровень изоляции транзакции для объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="7f721-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f721-105">Константа</span><span class="sxs-lookup"><span data-stu-id="7f721-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7f721-106">Значение</span><span class="sxs-lookup"><span data-stu-id="7f721-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7f721-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7f721-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f721-108"><strong>АдксактунспеЦифиед</strong></span><span class="sxs-lookup"><span data-stu-id="7f721-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="7f721-109">–1</span><span class="sxs-lookup"><span data-stu-id="7f721-109">-1</span></span></p></td>
<td><p><span data-ttu-id="7f721-110">Указывает, что поставщик использует уровень изоляции, отличный от указанного, но уровень не может быть определен.</span><span class="sxs-lookup"><span data-stu-id="7f721-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f721-111"><strong>Адксактчаос</strong></span><span class="sxs-lookup"><span data-stu-id="7f721-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="7f721-112">столбцов</span><span class="sxs-lookup"><span data-stu-id="7f721-112">16</span></span></p></td>
<td><p><span data-ttu-id="7f721-113">Указывает, что ожидающие изменения более изолированных транзакций не могут быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="7f721-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f721-114"><strong>Адксактбровсе</strong></span><span class="sxs-lookup"><span data-stu-id="7f721-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="7f721-115">256</span><span class="sxs-lookup"><span data-stu-id="7f721-115">256</span></span></p></td>
<td><p><span data-ttu-id="7f721-116">Указывает, что из одной транзакции можно просматривать незафиксированные изменения в других транзакциях.</span><span class="sxs-lookup"><span data-stu-id="7f721-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f721-117"><strong>Адксактреадункоммиттед</strong></span><span class="sxs-lookup"><span data-stu-id="7f721-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="7f721-118">256</span><span class="sxs-lookup"><span data-stu-id="7f721-118">256</span></span></p></td>
<td><p><span data-ttu-id="7f721-119">То же, что и <strong>адксактбровсе</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f721-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f721-120"><strong>Адксакткурсорстабилити</strong></span><span class="sxs-lookup"><span data-stu-id="7f721-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="7f721-121">4096</span><span class="sxs-lookup"><span data-stu-id="7f721-121">4096</span></span></p></td>
<td><p><span data-ttu-id="7f721-122">Указывает, что из одной транзакции вы можете просматривать изменения в других транзакциях только после того, как они были зафиксированы.</span><span class="sxs-lookup"><span data-stu-id="7f721-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f721-123"><strong>Адксактреадкоммиттед</strong></span><span class="sxs-lookup"><span data-stu-id="7f721-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="7f721-124">4096</span><span class="sxs-lookup"><span data-stu-id="7f721-124">4096</span></span></p></td>
<td><p><span data-ttu-id="7f721-125">То же, что и <strong>адксакткурсорстабилити</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f721-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f721-126"><strong>Адксактрепеатаблереад</strong></span><span class="sxs-lookup"><span data-stu-id="7f721-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="7f721-127">65536</span><span class="sxs-lookup"><span data-stu-id="7f721-127">65536</span></span></p></td>
<td><p><span data-ttu-id="7f721-128">Указывает, что из одной транзакции невозможно увидеть изменения, внесенные в другие транзакции, но это может привести к извлечению новых объектов <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="7f721-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f721-129"><strong>Адксактисолатед</strong></span><span class="sxs-lookup"><span data-stu-id="7f721-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="7f721-130">1048576</span><span class="sxs-lookup"><span data-stu-id="7f721-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="7f721-131">Указывает на то, что транзакции проведены в изоляции других транзакций.</span><span class="sxs-lookup"><span data-stu-id="7f721-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f721-132"><strong>Адксактсериализабле</strong></span><span class="sxs-lookup"><span data-stu-id="7f721-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="7f721-133">1048576</span><span class="sxs-lookup"><span data-stu-id="7f721-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="7f721-134">То же, что и <strong>адксактисолатед</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f721-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="7f721-135">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="7f721-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="7f721-136">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="7f721-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f721-137">Константа</span><span class="sxs-lookup"><span data-stu-id="7f721-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f721-138">Адоенумс. IsolationLevel. unspecifieded</span><span class="sxs-lookup"><span data-stu-id="7f721-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f721-139">Адоенумс. IsolationLevel. беспорядок</span><span class="sxs-lookup"><span data-stu-id="7f721-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f721-140">Адоенумс. IsolationLevel. BROWSE</span><span class="sxs-lookup"><span data-stu-id="7f721-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f721-141">Адоенумс. IsolationLevel. РЕАДУНКОММИТТЕД</span><span class="sxs-lookup"><span data-stu-id="7f721-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f721-142">Адоенумс. IsolationLevel. КУРСОРСТАБИЛИТИ</span><span class="sxs-lookup"><span data-stu-id="7f721-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f721-143">Адоенумс. IsolationLevel. РЕАДКОММИТТЕД</span><span class="sxs-lookup"><span data-stu-id="7f721-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f721-144">Адоенумс. IsolationLevel. РЕПЕАТАБЛЕРЕАД</span><span class="sxs-lookup"><span data-stu-id="7f721-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f721-145">Адоенумс. IsolationLevel. изоляция</span><span class="sxs-lookup"><span data-stu-id="7f721-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f721-146">Адоенумс. IsolationLevel. SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="7f721-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

