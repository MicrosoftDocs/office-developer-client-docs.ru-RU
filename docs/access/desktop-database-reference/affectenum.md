---
title: AffectEnum (Справочник по для настольных баз данных Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9725a0e4af6ac6d25140739d6604abae6b76dcb6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879447"
---
# <a name="affectenum"></a><span data-ttu-id="fc9d1-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="fc9d1-102">AffectEnum</span></span>

<span data-ttu-id="fc9d1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc9d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc9d1-104">Указывает, какие записи, влияют операции.</span><span class="sxs-lookup"><span data-stu-id="fc9d1-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc9d1-105">Константа</span><span class="sxs-lookup"><span data-stu-id="fc9d1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fc9d1-106">Значение</span><span class="sxs-lookup"><span data-stu-id="fc9d1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fc9d1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fc9d1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc9d1-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="fc9d1-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="fc9d1-109">3</span><span class="sxs-lookup"><span data-stu-id="fc9d1-109">3</span></span></p></td>
<td><p><span data-ttu-id="fc9d1-110">Если не применен <a href="filter-property-ado.md">Фильтр</a> для <strong>записей</strong>, влияет на все записи.</span><span class="sxs-lookup"><span data-stu-id="fc9d1-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="fc9d1-111">Если свойство <strong>фильтра</strong> имеет значение условий строки (например, &quot;автор = «Smith»&quot;), операцию влияет на видимых записей в текущем.</span><span class="sxs-lookup"><span data-stu-id="fc9d1-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="fc9d1-112">Если свойство <strong>фильтра</strong> должна быть членом <a href="filtergroupenum.md">FilterGroupEnum</a> или массив закладки, операция повлияет на все строки из <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc9d1-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p>
<p><span data-ttu-id="fc9d1-113"><strong>Примечание</strong>: adAffectAll скрыто в обозревателе объектов Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fc9d1-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc9d1-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="fc9d1-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="fc9d1-115">4</span><span class="sxs-lookup"><span data-stu-id="fc9d1-115">4</span></span></p></td>
<td><p><span data-ttu-id="fc9d1-116">Влияет на все записи в все родственные главы набора <strong>записей</strong>, включая те, которые не видны с помощью любого <strong>фильтра</strong> , применяемого в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="fc9d1-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc9d1-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="fc9d1-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="fc9d1-118">1</span><span class="sxs-lookup"><span data-stu-id="fc9d1-118">1</span></span></p></td>
<td><p><span data-ttu-id="fc9d1-119">Влияет только текущей записи.</span><span class="sxs-lookup"><span data-stu-id="fc9d1-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc9d1-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="fc9d1-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="fc9d1-121">2</span><span class="sxs-lookup"><span data-stu-id="fc9d1-121">2</span></span></p></td>
<td><p><span data-ttu-id="fc9d1-122">Влияет только записи, которые удовлетворяют текущего значения свойства <a href="filter-property-ado.md">фильтра</a> .</span><span class="sxs-lookup"><span data-stu-id="fc9d1-122">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting.</span></span> <span data-ttu-id="fc9d1-123">Значение <strong>FilterGroupEnum</strong> или массив <strong>закладки</strong> , чтобы использовать этот параметр, необходимо установить свойство <strong>фильтра</strong> .</span><span class="sxs-lookup"><span data-stu-id="fc9d1-123">You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="fc9d1-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="fc9d1-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="fc9d1-125">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="fc9d1-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc9d1-126">Constant</span><span class="sxs-lookup"><span data-stu-id="fc9d1-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc9d1-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="fc9d1-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc9d1-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="fc9d1-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc9d1-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="fc9d1-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc9d1-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="fc9d1-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

