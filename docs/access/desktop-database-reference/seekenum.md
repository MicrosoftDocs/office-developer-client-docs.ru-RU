---
title: Сикенум (Справочник по базам данных Access на компьютере)
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
# <a name="seekenum"></a><span data-ttu-id="52bb3-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="52bb3-102">SeekEnum</span></span>

<span data-ttu-id="52bb3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52bb3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52bb3-104">Указывает тип выполняемого [поиска](seek-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="52bb3-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52bb3-105">Константа</span><span class="sxs-lookup"><span data-stu-id="52bb3-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="52bb3-106">Значение</span><span class="sxs-lookup"><span data-stu-id="52bb3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="52bb3-107">Описание</span><span class="sxs-lookup"><span data-stu-id="52bb3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52bb3-108">Адсикфирстек</span><span class="sxs-lookup"><span data-stu-id="52bb3-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="52bb3-109">1,1</span><span class="sxs-lookup"><span data-stu-id="52bb3-109">1</span></span></p></td>
<td><p><span data-ttu-id="52bb3-110">Ищет первый ключ, равный <em>кэйвалуес</em>.</span><span class="sxs-lookup"><span data-stu-id="52bb3-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52bb3-111">Адсикластек</span><span class="sxs-lookup"><span data-stu-id="52bb3-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="52bb3-112">2</span><span class="sxs-lookup"><span data-stu-id="52bb3-112">2</span></span></p></td>
<td><p><span data-ttu-id="52bb3-113">Ищет последний ключ, равный <em>кэйвалуес</em>.</span><span class="sxs-lookup"><span data-stu-id="52bb3-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52bb3-114">Адсикафтерек</span><span class="sxs-lookup"><span data-stu-id="52bb3-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="52bb3-115">SP4</span><span class="sxs-lookup"><span data-stu-id="52bb3-115">4</span></span></p></td>
<td><p><span data-ttu-id="52bb3-116">Ищет ключ, равный <em>кэйвалуес</em> , или сразу после того, как будет выполнено совпадение.</span><span class="sxs-lookup"><span data-stu-id="52bb3-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52bb3-117">Адсикафтер</span><span class="sxs-lookup"><span data-stu-id="52bb3-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="52bb3-118">8,5</span><span class="sxs-lookup"><span data-stu-id="52bb3-118">8</span></span></p></td>
<td><p><span data-ttu-id="52bb3-119">Ищет ключ сразу после того места, где произошло сравнение с <em>кэйвалуес</em> .</span><span class="sxs-lookup"><span data-stu-id="52bb3-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52bb3-120">Адсикбефорик</span><span class="sxs-lookup"><span data-stu-id="52bb3-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="52bb3-121">столбцов</span><span class="sxs-lookup"><span data-stu-id="52bb3-121">16</span></span></p></td>
<td><p><span data-ttu-id="52bb3-122">Ищет ключ, равный <em>кэйвалуес</em> , или только до того места, где будет выполнено это совпадение.</span><span class="sxs-lookup"><span data-stu-id="52bb3-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52bb3-123">Адсикбефоре</span><span class="sxs-lookup"><span data-stu-id="52bb3-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="52bb3-124">32</span><span class="sxs-lookup"><span data-stu-id="52bb3-124">32</span></span></p></td>
<td><p><span data-ttu-id="52bb3-125">Ищет ключ до того места, где было бы обнаружено сравнение с <em>кэйвалуес</em> .</span><span class="sxs-lookup"><span data-stu-id="52bb3-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="52bb3-126">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="52bb3-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="52bb3-127">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="52bb3-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52bb3-128">Константа</span><span class="sxs-lookup"><span data-stu-id="52bb3-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52bb3-129">Адоенумс. Seek. ФИРСТЕК</span><span class="sxs-lookup"><span data-stu-id="52bb3-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52bb3-130">Адоенумс. Seek. ЛАСТЕК</span><span class="sxs-lookup"><span data-stu-id="52bb3-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52bb3-131">Адоенумс. Seek. АФТЕРЕК</span><span class="sxs-lookup"><span data-stu-id="52bb3-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52bb3-132">Адоенумс. Seek. AFTER</span><span class="sxs-lookup"><span data-stu-id="52bb3-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52bb3-133">Адоенумс. Seek. БЕФОРИК</span><span class="sxs-lookup"><span data-stu-id="52bb3-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52bb3-134">Адоенумс. Seek. BEFORE</span><span class="sxs-lookup"><span data-stu-id="52bb3-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

