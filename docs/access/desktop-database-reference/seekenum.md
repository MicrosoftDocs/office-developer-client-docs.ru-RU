---
title: SeekEnum (Ссылка на настольные базы данных)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314660"
---
# <a name="seekenum"></a><span data-ttu-id="6fabe-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="6fabe-102">SeekEnum</span></span>

<span data-ttu-id="6fabe-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fabe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6fabe-104">Указывает тип [поиска](seek-method-ado.md) для выполнения.</span><span class="sxs-lookup"><span data-stu-id="6fabe-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fabe-105">Константа</span><span class="sxs-lookup"><span data-stu-id="6fabe-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6fabe-106">Значение</span><span class="sxs-lookup"><span data-stu-id="6fabe-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6fabe-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6fabe-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fabe-108">adSeekFirstEQ</span><span class="sxs-lookup"><span data-stu-id="6fabe-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="6fabe-109">1</span><span class="sxs-lookup"><span data-stu-id="6fabe-109">1</span></span></p></td>
<td><p><span data-ttu-id="6fabe-110">Ищет первый ключ, равный <em>KeyValues.</em></span><span class="sxs-lookup"><span data-stu-id="6fabe-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fabe-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="6fabe-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="6fabe-112">2</span><span class="sxs-lookup"><span data-stu-id="6fabe-112">2</span></span></p></td>
<td><p><span data-ttu-id="6fabe-113">Ищет последний ключ, равный <em>KeyValues.</em></span><span class="sxs-lookup"><span data-stu-id="6fabe-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fabe-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="6fabe-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="6fabe-115">4 </span><span class="sxs-lookup"><span data-stu-id="6fabe-115">4</span></span></p></td>
<td><p><span data-ttu-id="6fabe-116">Ищет ключ, равный <em>KeyValues,</em> или сразу после того, где это совпадение произошло бы.</span><span class="sxs-lookup"><span data-stu-id="6fabe-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fabe-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="6fabe-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="6fabe-118">8 </span><span class="sxs-lookup"><span data-stu-id="6fabe-118">8</span></span></p></td>
<td><p><span data-ttu-id="6fabe-119">Ищет ключ сразу после совпадения с <em>KeyValues.</em></span><span class="sxs-lookup"><span data-stu-id="6fabe-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fabe-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="6fabe-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="6fabe-121">16 </span><span class="sxs-lookup"><span data-stu-id="6fabe-121">16</span></span></p></td>
<td><p><span data-ttu-id="6fabe-122">Ищет ключ, равный <em>KeyValues,</em> или как раз перед тем, где это совпадение произошло бы.</span><span class="sxs-lookup"><span data-stu-id="6fabe-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fabe-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="6fabe-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="6fabe-124">32</span><span class="sxs-lookup"><span data-stu-id="6fabe-124">32</span></span></p></td>
<td><p><span data-ttu-id="6fabe-125">Ищет ключ перед началом совпадения с <em>KeyValues.</em></span><span class="sxs-lookup"><span data-stu-id="6fabe-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6fabe-126">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="6fabe-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="6fabe-127">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6fabe-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fabe-128">Константа</span><span class="sxs-lookup"><span data-stu-id="6fabe-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fabe-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="6fabe-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fabe-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="6fabe-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fabe-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="6fabe-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fabe-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="6fabe-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fabe-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="6fabe-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fabe-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="6fabe-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

