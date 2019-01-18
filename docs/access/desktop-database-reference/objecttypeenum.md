---
title: ObjectTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e3b470c8c0d0c3f04b59bd382b66117bd79c188
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711835"
---
# <a name="objecttypeenum"></a><span data-ttu-id="8b950-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="8b950-102">ObjectTypeEnum</span></span>

<span data-ttu-id="8b950-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b950-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b950-104">Указывает тип объекта базы данных, для которого необходимо задать разрешения или владельца.</span><span class="sxs-lookup"><span data-stu-id="8b950-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b950-105">Константа</span><span class="sxs-lookup"><span data-stu-id="8b950-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8b950-106">Значение</span><span class="sxs-lookup"><span data-stu-id="8b950-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8b950-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8b950-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b950-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="8b950-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="8b950-109">2</span><span class="sxs-lookup"><span data-stu-id="8b950-109">2</span></span></p></td>
<td><p><span data-ttu-id="8b950-110">Объект является столбец.</span><span class="sxs-lookup"><span data-stu-id="8b950-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b950-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="8b950-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="8b950-112">3</span><span class="sxs-lookup"><span data-stu-id="8b950-112">3</span></span></p></td>
<td><p><span data-ttu-id="8b950-113">Объект представляет собой базу данных.</span><span class="sxs-lookup"><span data-stu-id="8b950-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b950-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="8b950-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="8b950-115">4</span><span class="sxs-lookup"><span data-stu-id="8b950-115">4</span></span></p></td>
<td><p><span data-ttu-id="8b950-116">Объект не является процедурой.</span><span class="sxs-lookup"><span data-stu-id="8b950-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b950-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="8b950-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="8b950-118">–1</span><span class="sxs-lookup"><span data-stu-id="8b950-118">-1</span></span></p></td>
<td><p><span data-ttu-id="8b950-119">Объект — это тип, определяемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="8b950-119">The object is a type defined by the provider.</span></span> <span data-ttu-id="8b950-120">Если параметр <em>ObjectType</em> <strong>adPermObjProviderSpecific</strong> и <em>ObjectTypeId</em> не указан, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="8b950-120">An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b950-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="8b950-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="8b950-122">1</span><span class="sxs-lookup"><span data-stu-id="8b950-122">1</span></span></p></td>
<td><p><span data-ttu-id="8b950-123">Объект — это таблица.</span><span class="sxs-lookup"><span data-stu-id="8b950-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b950-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="8b950-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="8b950-125">5</span><span class="sxs-lookup"><span data-stu-id="8b950-125">5</span></span></p></td>
<td><p><span data-ttu-id="8b950-126">Объект — это представление.</span><span class="sxs-lookup"><span data-stu-id="8b950-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

