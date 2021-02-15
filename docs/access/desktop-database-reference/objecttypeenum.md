---
title: ObjectTypeEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e3b470c8c0d0c3f04b59bd382b66117bd79c188
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288534"
---
# <a name="objecttypeenum"></a><span data-ttu-id="a9fa8-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="a9fa8-102">ObjectTypeEnum</span></span>

<span data-ttu-id="a9fa8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9fa8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9fa8-104">Указывает тип объекта базы данных, для которого необходимо установить разрешения или права владельца.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9fa8-105">Константа</span><span class="sxs-lookup"><span data-stu-id="a9fa8-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a9fa8-106">Значение</span><span class="sxs-lookup"><span data-stu-id="a9fa8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a9fa8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a9fa8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9fa8-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="a9fa8-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="a9fa8-109">2 </span><span class="sxs-lookup"><span data-stu-id="a9fa8-109">2</span></span></p></td>
<td><p><span data-ttu-id="a9fa8-110">Объект является столбцом.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9fa8-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="a9fa8-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="a9fa8-112">3 </span><span class="sxs-lookup"><span data-stu-id="a9fa8-112">3</span></span></p></td>
<td><p><span data-ttu-id="a9fa8-113">Объект является базой данных.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9fa8-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="a9fa8-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="a9fa8-115">4 </span><span class="sxs-lookup"><span data-stu-id="a9fa8-115">4</span></span></p></td>
<td><p><span data-ttu-id="a9fa8-116">Объект является процедурой.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9fa8-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="a9fa8-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="a9fa8-118">–1</span><span class="sxs-lookup"><span data-stu-id="a9fa8-118">-1</span></span></p></td>
<td><p><span data-ttu-id="a9fa8-119">Объект — это тип, определенный поставщиком.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-119">The object is a type defined by the provider.</span></span> <span data-ttu-id="a9fa8-120">Если параметр <em>ObjectType</em> имеет тип <strong>adPermObjProviderSpecific</strong> и <em>ObjectTypeId</em> не задан, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-120">An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9fa8-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="a9fa8-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="a9fa8-122">1 </span><span class="sxs-lookup"><span data-stu-id="a9fa8-122">1</span></span></p></td>
<td><p><span data-ttu-id="a9fa8-123">Объект является таблицей.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9fa8-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="a9fa8-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="a9fa8-125">5 </span><span class="sxs-lookup"><span data-stu-id="a9fa8-125">5</span></span></p></td>
<td><p><span data-ttu-id="a9fa8-126">Объект — это представление.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

