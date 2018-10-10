---
title: AffectEnum (Справочник по для настольных баз данных Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ffb2ab2abbd24a19ddc433b5fd315dd535fd2a0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481002"
---
# <a name="affectenum"></a><span data-ttu-id="700a9-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="700a9-102">AffectEnum</span></span>


<span data-ttu-id="700a9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="700a9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="700a9-104">Указывает, какие записи, влияют операции.</span><span class="sxs-lookup"><span data-stu-id="700a9-104">Specifies which records are affected by an operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="700a9-105">Константа</span><span class="sxs-lookup"><span data-stu-id="700a9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="700a9-106">Значение</span><span class="sxs-lookup"><span data-stu-id="700a9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="700a9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="700a9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="700a9-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="700a9-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="700a9-109">3</span><span class="sxs-lookup"><span data-stu-id="700a9-109">3</span></span></p></td>
<td><p><span data-ttu-id="700a9-110">Если не применен <a href="filter-property-ado.md">Фильтр</a> для <strong>записей</strong>, влияет на все записи.</span><span class="sxs-lookup"><span data-stu-id="700a9-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="700a9-111">Если свойство <strong>фильтра</strong> имеет значение условий строки (таких как &quot;автор = «Smith»&quot;), а затем операцию влияет на видимых записей в текущем.</span><span class="sxs-lookup"><span data-stu-id="700a9-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), then the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="700a9-112">Если свойство <strong>фильтра</strong> должна быть членом <a href="filtergroupenum.md">FilterGroupEnum</a> или массив закладки, операция затронет все строки из <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="700a9-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, then the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="700a9-113">adAffectAll является скрытым в обозревателе объектов Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="700a9-113">adAffectAll is hidden in the Visual Basic Object Browser.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="700a9-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="700a9-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="700a9-115">4</span><span class="sxs-lookup"><span data-stu-id="700a9-115">4</span></span></p></td>
<td><p><span data-ttu-id="700a9-116">Влияет на все записи в все родственные главы набора <strong>записей</strong>, включая те, которые не видны с помощью любого <strong>фильтра</strong> , применяемого в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="700a9-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="700a9-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="700a9-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="700a9-118">1</span><span class="sxs-lookup"><span data-stu-id="700a9-118">1</span></span></p></td>
<td><p><span data-ttu-id="700a9-119">Влияет только текущей записи.</span><span class="sxs-lookup"><span data-stu-id="700a9-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="700a9-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="700a9-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="700a9-121">2</span><span class="sxs-lookup"><span data-stu-id="700a9-121">2</span></span></p></td>
<td><p><span data-ttu-id="700a9-122">Влияет только записи, которые удовлетворяют текущего значения свойства <a href="filter-property-ado.md">фильтра</a> .</span><span class="sxs-lookup"><span data-stu-id="700a9-122">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting.</span></span> <span data-ttu-id="700a9-123">Значение <strong>FilterGroupEnum</strong> или массив <strong>закладки</strong> , чтобы использовать этот параметр, необходимо установить свойство <strong>фильтра</strong> .</span><span class="sxs-lookup"><span data-stu-id="700a9-123">You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="700a9-124">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="700a9-124">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="700a9-125">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="700a9-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="700a9-126">Constant</span><span class="sxs-lookup"><span data-stu-id="700a9-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="700a9-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="700a9-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="700a9-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="700a9-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="700a9-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="700a9-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="700a9-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="700a9-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

