---
title: SeekEnum (Справочник по для настольных баз данных Access)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698612"
---
# <a name="seekenum"></a><span data-ttu-id="98b4d-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="98b4d-102">SeekEnum</span></span>

<span data-ttu-id="98b4d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98b4d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98b4d-104">Указывает тип [поиска](seek-method-ado.md) для выполнения.</span><span class="sxs-lookup"><span data-stu-id="98b4d-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98b4d-105">Константа</span><span class="sxs-lookup"><span data-stu-id="98b4d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="98b4d-106">Значение</span><span class="sxs-lookup"><span data-stu-id="98b4d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="98b4d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="98b4d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98b4d-108">adSeekFirstEQ</span><span class="sxs-lookup"><span data-stu-id="98b4d-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="98b4d-109">1</span><span class="sxs-lookup"><span data-stu-id="98b4d-109">1</span></span></p></td>
<td><p><span data-ttu-id="98b4d-110">Выполняет поиск первого параметра значения для <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="98b4d-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98b4d-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="98b4d-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="98b4d-112">2</span><span class="sxs-lookup"><span data-stu-id="98b4d-112">2</span></span></p></td>
<td><p><span data-ttu-id="98b4d-113">Выполняет поиск последнего ключа равно <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="98b4d-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98b4d-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="98b4d-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="98b4d-115">4</span><span class="sxs-lookup"><span data-stu-id="98b4d-115">4</span></span></p></td>
<td><p><span data-ttu-id="98b4d-116">Выполняет поиск параметра значения, чтобы <em>KeyValues</em> или сразу после которых выполнялось, соответствующими.</span><span class="sxs-lookup"><span data-stu-id="98b4d-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98b4d-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="98b4d-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="98b4d-118">8</span><span class="sxs-lookup"><span data-stu-id="98b4d-118">8</span></span></p></td>
<td><p><span data-ttu-id="98b4d-119">Сразу после которых выполнялось совпадение с <em>KeyValues</em> операций поиска ключа.</span><span class="sxs-lookup"><span data-stu-id="98b4d-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98b4d-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="98b4d-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="98b4d-121">16</span><span class="sxs-lookup"><span data-stu-id="98b4d-121">16</span></span></p></td>
<td><p><span data-ttu-id="98b4d-122">Выполняет поиск параметра значения, чтобы <em>KeyValues</em> или непосредственно перед которых выполнялось, соответствующие.</span><span class="sxs-lookup"><span data-stu-id="98b4d-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98b4d-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="98b4d-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="98b4d-124">32</span><span class="sxs-lookup"><span data-stu-id="98b4d-124">32</span></span></p></td>
<td><p><span data-ttu-id="98b4d-125">Выполняет поиск ключа перед которых выполнялось совпадение с <em>KeyValues</em> .</span><span class="sxs-lookup"><span data-stu-id="98b4d-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="98b4d-126">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="98b4d-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="98b4d-127">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="98b4d-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98b4d-128">Константа</span><span class="sxs-lookup"><span data-stu-id="98b4d-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98b4d-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="98b4d-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98b4d-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="98b4d-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98b4d-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="98b4d-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98b4d-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="98b4d-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98b4d-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="98b4d-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98b4d-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="98b4d-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

