---
title: AffectEnum (Ссылка на настольные базы данных)
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
# <a name="affectenum"></a><span data-ttu-id="37cf4-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="37cf4-102">AffectEnum</span></span>

<span data-ttu-id="37cf4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37cf4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37cf4-104">Указывает, на какие записи влияет операция.</span><span class="sxs-lookup"><span data-stu-id="37cf4-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37cf4-105">Константа</span><span class="sxs-lookup"><span data-stu-id="37cf4-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="37cf4-106">Значение</span><span class="sxs-lookup"><span data-stu-id="37cf4-106">Value</span></span></p></th>
<th><p><span data-ttu-id="37cf4-107">Описание</span><span class="sxs-lookup"><span data-stu-id="37cf4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37cf4-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="37cf4-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="37cf4-109">3</span><span class="sxs-lookup"><span data-stu-id="37cf4-109">3</span></span></p></td>
<td><p><span data-ttu-id="37cf4-110">Если фильтр не <a href="filter-property-ado.md">применяется</a> к <strong>Набору записей,</strong>влияет на все записи.</span><span class="sxs-lookup"><span data-stu-id="37cf4-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="37cf4-111">Если свойство <strong>Filter</strong> заданной для строки (например, Author='Smith), операция влияет на видимые записи &quot; в текущей &quot; главе.</span><span class="sxs-lookup"><span data-stu-id="37cf4-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="37cf4-112">Если свойство <strong>Filter</strong> установлено для члена <a href="filtergroupenum.md">FilterGroupEnum</a> или массива закладок, операция затронет все строки <strong>набора записей.</strong></span><span class="sxs-lookup"><span data-stu-id="37cf4-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="37cf4-113"><strong>ПРИМЕЧАНИЕ.</strong>adAffectAll скрыт в браузере Visual Basic объекта.</span><span class="sxs-lookup"><span data-stu-id="37cf4-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37cf4-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="37cf4-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="37cf4-115">4 </span><span class="sxs-lookup"><span data-stu-id="37cf4-115">4</span></span></p></td>
<td><p><span data-ttu-id="37cf4-116">Влияет на все записи во всех главах <strong>наборов</strong>записей, включая записи, которые не видны с помощью фильтра, <strong>который</strong> применяется в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="37cf4-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37cf4-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="37cf4-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="37cf4-118">1</span><span class="sxs-lookup"><span data-stu-id="37cf4-118">1</span></span></p></td>
<td><p><span data-ttu-id="37cf4-119">Влияет только на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="37cf4-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37cf4-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="37cf4-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="37cf4-121">2</span><span class="sxs-lookup"><span data-stu-id="37cf4-121">2</span></span></p></td>
<td><p><span data-ttu-id="37cf4-122">Влияет только на записи, удовлетворяющие текущему <a href="filter-property-ado.md">параметру свойства Filter.</a></span><span class="sxs-lookup"><span data-stu-id="37cf4-122">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting.</span></span> <span data-ttu-id="37cf4-123">Для использования <strong>этого</strong> параметра необходимо указать свойство Filter <strong></strong> значение <strong>FilterGroupEnum</strong> или массив закладок.</span><span class="sxs-lookup"><span data-stu-id="37cf4-123">You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="37cf4-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="37cf4-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="37cf4-125">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="37cf4-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37cf4-126">Константа</span><span class="sxs-lookup"><span data-stu-id="37cf4-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37cf4-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="37cf4-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37cf4-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="37cf4-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37cf4-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="37cf4-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37cf4-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="37cf4-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

