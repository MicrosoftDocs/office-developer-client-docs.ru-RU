---
title: Компаринум (Справочник по базам данных Access на компьютере)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd120f726a51c884d063bb03f6d6864ea2d48344
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296068"
---
# <a name="compareenum"></a><span data-ttu-id="670e5-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="670e5-102">CompareEnum</span></span>

<span data-ttu-id="670e5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="670e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="670e5-104">Задает относительное положение двух записей, представленных в закладках.</span><span class="sxs-lookup"><span data-stu-id="670e5-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="670e5-105">Константа</span><span class="sxs-lookup"><span data-stu-id="670e5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="670e5-106">Значение</span><span class="sxs-lookup"><span data-stu-id="670e5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="670e5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="670e5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="670e5-108"><strong>адкомпарикуал</strong></span><span class="sxs-lookup"><span data-stu-id="670e5-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="670e5-109">1,1</span><span class="sxs-lookup"><span data-stu-id="670e5-109">1</span></span></p></td>
<td><p><span data-ttu-id="670e5-110">Указывает, что закладки совпадают.</span><span class="sxs-lookup"><span data-stu-id="670e5-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="670e5-111"><strong>адкомпарегреатерсан</strong></span><span class="sxs-lookup"><span data-stu-id="670e5-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="670e5-112">2</span><span class="sxs-lookup"><span data-stu-id="670e5-112">2</span></span></p></td>
<td><p><span data-ttu-id="670e5-113">Указывает, что первая закладка находится после секунды.</span><span class="sxs-lookup"><span data-stu-id="670e5-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="670e5-114"><strong>адкомпарелесссан</strong></span><span class="sxs-lookup"><span data-stu-id="670e5-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="670e5-115">нуль</span><span class="sxs-lookup"><span data-stu-id="670e5-115">0</span></span></p></td>
<td><p><span data-ttu-id="670e5-116">Указывает, что первая закладка предшествует второй.</span><span class="sxs-lookup"><span data-stu-id="670e5-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="670e5-117"><strong>адкомпареноткомпарабле</strong></span><span class="sxs-lookup"><span data-stu-id="670e5-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="670e5-118">4 </span><span class="sxs-lookup"><span data-stu-id="670e5-118">4</span></span></p></td>
<td><p><span data-ttu-id="670e5-119">Указывает, что закладки невозможно сравнить.</span><span class="sxs-lookup"><span data-stu-id="670e5-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="670e5-120"><strong>адкомпаренотекуал</strong></span><span class="sxs-lookup"><span data-stu-id="670e5-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="670e5-121">4</span><span class="sxs-lookup"><span data-stu-id="670e5-121">3</span></span></p></td>
<td><p><span data-ttu-id="670e5-122">Указывает, что закладки не равны и не упорядочены.</span><span class="sxs-lookup"><span data-stu-id="670e5-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="670e5-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="670e5-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="670e5-124">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="670e5-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="670e5-125">Константа</span><span class="sxs-lookup"><span data-stu-id="670e5-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="670e5-126">Адоенумс. Compare. EQUALs</span><span class="sxs-lookup"><span data-stu-id="670e5-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="670e5-127">Адоенумс. Compare. GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="670e5-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="670e5-128">Адоенумс. Compare. ЛЕСССАН</span><span class="sxs-lookup"><span data-stu-id="670e5-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="670e5-129">Адоенумс. Compare. НОТКОМПАРАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="670e5-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="670e5-130">Адоенумс. Compare. NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="670e5-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

