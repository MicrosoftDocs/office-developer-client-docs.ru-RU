---
title: AffectEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297202"
---
# <a name="affectenum"></a><span data-ttu-id="18b74-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="18b74-102">AffectEnum</span></span>

<span data-ttu-id="18b74-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18b74-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18b74-104">Указывает, на какие записи влияет операция.</span><span class="sxs-lookup"><span data-stu-id="18b74-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18b74-105">Константа</span><span class="sxs-lookup"><span data-stu-id="18b74-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="18b74-106">Значение</span><span class="sxs-lookup"><span data-stu-id="18b74-106">Value</span></span></p></th>
<th><p><span data-ttu-id="18b74-107">Описание</span><span class="sxs-lookup"><span data-stu-id="18b74-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18b74-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="18b74-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="18b74-109">3 </span><span class="sxs-lookup"><span data-stu-id="18b74-109">3</span></span></p></td>
<td><p><span data-ttu-id="18b74-110">Если к набору <a href="filter-property-ado.md">записей не</a> применяется <strong>фильтр,</strong>это влияет на все записи.</span><span class="sxs-lookup"><span data-stu-id="18b74-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="18b74-111">Если свойство <strong>Filter</strong> имеет строку условия (например, Author='Smith'), операция влияет на видимые записи &quot; &quot; в текущей главе.</span><span class="sxs-lookup"><span data-stu-id="18b74-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="18b74-112">Если для <strong>свойства Filter</strong> установлено свойство <a href="filtergroupenum.md">FilterGroupEnum</a> или массив закладок, операция повлияет на все строки <strong>набора записей.</strong></span><span class="sxs-lookup"><span data-stu-id="18b74-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="18b74-113"><strong>ПРИМЕЧАНИЕ.</strong>AdAffectAll скрыт в браузере Visual Basic объектов.</span><span class="sxs-lookup"><span data-stu-id="18b74-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b74-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="18b74-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="18b74-115">4 </span><span class="sxs-lookup"><span data-stu-id="18b74-115">4</span></span></p></td>
<td><p><span data-ttu-id="18b74-116">Влияет на все записи во всех <strong></strong>главах одного и того же раздела в наборе записей, включая те, которые не видны с помощью <strong>фильтра,</strong> который применяется в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="18b74-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18b74-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="18b74-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="18b74-118">1 </span><span class="sxs-lookup"><span data-stu-id="18b74-118">1</span></span></p></td>
<td><p><span data-ttu-id="18b74-119">Влияет только на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="18b74-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b74-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="18b74-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="18b74-121">2 </span><span class="sxs-lookup"><span data-stu-id="18b74-121">2</span></span></p></td>
<td><p><span data-ttu-id="18b74-122">Влияет только на записи, удовлетворяющие <a href="filter-property-ado.md">текущему параметру</a> свойства Filter.</span><span class="sxs-lookup"><span data-stu-id="18b74-122">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting.</span></span> <span data-ttu-id="18b74-123">Чтобы использовать этот <strong>параметр,</strong> необходимо установить для свойства <strong></strong> <strong>Filter значение FilterGroupEnum</strong> или массив закладок.</span><span class="sxs-lookup"><span data-stu-id="18b74-123">You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="18b74-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="18b74-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="18b74-125">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="18b74-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18b74-126">Константа</span><span class="sxs-lookup"><span data-stu-id="18b74-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18b74-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="18b74-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b74-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="18b74-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18b74-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="18b74-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b74-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="18b74-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

