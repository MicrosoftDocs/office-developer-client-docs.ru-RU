---
title: CompareEnum (справочник по базе данных Access для настольных ПК)
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
# <a name="compareenum"></a><span data-ttu-id="efcec-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="efcec-102">CompareEnum</span></span>

<span data-ttu-id="efcec-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="efcec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="efcec-104">Указывает относительное положение двух записей, представленных закладки.</span><span class="sxs-lookup"><span data-stu-id="efcec-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="efcec-105">Константа</span><span class="sxs-lookup"><span data-stu-id="efcec-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="efcec-106">Значение</span><span class="sxs-lookup"><span data-stu-id="efcec-106">Value</span></span></p></th>
<th><p><span data-ttu-id="efcec-107">Описание</span><span class="sxs-lookup"><span data-stu-id="efcec-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efcec-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="efcec-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="efcec-109">1 </span><span class="sxs-lookup"><span data-stu-id="efcec-109">1</span></span></p></td>
<td><p><span data-ttu-id="efcec-110">Указывает, что закладки равны.</span><span class="sxs-lookup"><span data-stu-id="efcec-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcec-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="efcec-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="efcec-112">2 </span><span class="sxs-lookup"><span data-stu-id="efcec-112">2</span></span></p></td>
<td><p><span data-ttu-id="efcec-113">Указывает, что первая закладка находится после второй.</span><span class="sxs-lookup"><span data-stu-id="efcec-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcec-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="efcec-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="efcec-115">0</span><span class="sxs-lookup"><span data-stu-id="efcec-115">0</span></span></p></td>
<td><p><span data-ttu-id="efcec-116">Указывает, что первая закладка находится перед второй.</span><span class="sxs-lookup"><span data-stu-id="efcec-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcec-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="efcec-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="efcec-118">4 </span><span class="sxs-lookup"><span data-stu-id="efcec-118">4</span></span></p></td>
<td><p><span data-ttu-id="efcec-119">Указывает, что закладки невозможно сравнить.</span><span class="sxs-lookup"><span data-stu-id="efcec-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcec-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="efcec-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="efcec-121">3 </span><span class="sxs-lookup"><span data-stu-id="efcec-121">3</span></span></p></td>
<td><p><span data-ttu-id="efcec-122">Указывает, что закладки не равны и не упорядочены.</span><span class="sxs-lookup"><span data-stu-id="efcec-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="efcec-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="efcec-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="efcec-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="efcec-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="efcec-125">Константа</span><span class="sxs-lookup"><span data-stu-id="efcec-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efcec-126">AdoEnums.Compare.EQUAL</span><span class="sxs-lookup"><span data-stu-id="efcec-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcec-127">AdoEnums.Compare.GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="efcec-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcec-128">AdoEnums.Compare.LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="efcec-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efcec-129">AdoEnums.Compare.NOTCOMPARABLE</span><span class="sxs-lookup"><span data-stu-id="efcec-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efcec-130">AdoEnums.Compare.NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="efcec-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

