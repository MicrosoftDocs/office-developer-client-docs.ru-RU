---
title: CompareEnum (Справочник по для настольных баз данных Access)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd120f726a51c884d063bb03f6d6864ea2d48344
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718898"
---
# <a name="compareenum"></a><span data-ttu-id="27781-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="27781-102">CompareEnum</span></span>

<span data-ttu-id="27781-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27781-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27781-104">Задает относительное положение двух записей, представленное закладок.</span><span class="sxs-lookup"><span data-stu-id="27781-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27781-105">Константа</span><span class="sxs-lookup"><span data-stu-id="27781-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="27781-106">Значение</span><span class="sxs-lookup"><span data-stu-id="27781-106">Value</span></span></p></th>
<th><p><span data-ttu-id="27781-107">Описание</span><span class="sxs-lookup"><span data-stu-id="27781-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27781-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="27781-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="27781-109">1</span><span class="sxs-lookup"><span data-stu-id="27781-109">1</span></span></p></td>
<td><p><span data-ttu-id="27781-110">Указывает, что закладки равны.</span><span class="sxs-lookup"><span data-stu-id="27781-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27781-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="27781-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="27781-112">2</span><span class="sxs-lookup"><span data-stu-id="27781-112">2</span></span></p></td>
<td><p><span data-ttu-id="27781-113">Указывает, что первая закладка после секунды.</span><span class="sxs-lookup"><span data-stu-id="27781-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27781-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="27781-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="27781-115">0</span><span class="sxs-lookup"><span data-stu-id="27781-115">0</span></span></p></td>
<td><p><span data-ttu-id="27781-116">Указывает, что первая закладка перед второй.</span><span class="sxs-lookup"><span data-stu-id="27781-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27781-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="27781-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="27781-118">4</span><span class="sxs-lookup"><span data-stu-id="27781-118">4</span></span></p></td>
<td><p><span data-ttu-id="27781-119">Указывает, что нельзя сравнивать закладки.</span><span class="sxs-lookup"><span data-stu-id="27781-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27781-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="27781-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="27781-121">3</span><span class="sxs-lookup"><span data-stu-id="27781-121">3</span></span></p></td>
<td><p><span data-ttu-id="27781-122">Указывает, что закладки не равно и не упорядоченные.</span><span class="sxs-lookup"><span data-stu-id="27781-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="27781-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="27781-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="27781-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="27781-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27781-125">Константа</span><span class="sxs-lookup"><span data-stu-id="27781-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27781-126">AdoEnums.Compare.EQUAL</span><span class="sxs-lookup"><span data-stu-id="27781-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27781-127">AdoEnums.Compare.GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="27781-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27781-128">AdoEnums.Compare.LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="27781-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27781-129">AdoEnums.Compare.NOTCOMPARABLE</span><span class="sxs-lookup"><span data-stu-id="27781-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27781-130">AdoEnums.Compare.NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="27781-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

