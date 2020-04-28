---
title: Обжекттипинум (Справочник по базам данных Access на компьютере)
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
# <a name="objecttypeenum"></a><span data-ttu-id="3bf2c-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="3bf2c-102">ObjectTypeEnum</span></span>

<span data-ttu-id="3bf2c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bf2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bf2c-104">Указывает тип объекта базы данных, для которого необходимо задать разрешения или владельца.</span><span class="sxs-lookup"><span data-stu-id="3bf2c-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3bf2c-105">Константа</span><span class="sxs-lookup"><span data-stu-id="3bf2c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3bf2c-106">Значение</span><span class="sxs-lookup"><span data-stu-id="3bf2c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3bf2c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3bf2c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3bf2c-108"><strong>адпермобжколумн</strong></span><span class="sxs-lookup"><span data-stu-id="3bf2c-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="3bf2c-109">2</span><span class="sxs-lookup"><span data-stu-id="3bf2c-109">2</span></span></p></td>
<td><p><span data-ttu-id="3bf2c-110">Объект является столбцом.</span><span class="sxs-lookup"><span data-stu-id="3bf2c-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bf2c-111"><strong>адпермобждатабасе</strong></span><span class="sxs-lookup"><span data-stu-id="3bf2c-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="3bf2c-112">4</span><span class="sxs-lookup"><span data-stu-id="3bf2c-112">3</span></span></p></td>
<td><p><span data-ttu-id="3bf2c-113">Объект представляет собой базу данных.</span><span class="sxs-lookup"><span data-stu-id="3bf2c-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bf2c-114"><strong>адпермобжпроцедуре</strong></span><span class="sxs-lookup"><span data-stu-id="3bf2c-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="3bf2c-115">4 </span><span class="sxs-lookup"><span data-stu-id="3bf2c-115">4</span></span></p></td>
<td><p><span data-ttu-id="3bf2c-116">Объект является процедурой.</span><span class="sxs-lookup"><span data-stu-id="3bf2c-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bf2c-117"><strong>адпермобжпровидерспеЦифик</strong></span><span class="sxs-lookup"><span data-stu-id="3bf2c-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="3bf2c-118">–1</span><span class="sxs-lookup"><span data-stu-id="3bf2c-118">-1</span></span></p></td>
<td><p><span data-ttu-id="3bf2c-119">Объект является типом, определяемым поставщиком.</span><span class="sxs-lookup"><span data-stu-id="3bf2c-119">The object is a type defined by the provider.</span></span> <span data-ttu-id="3bf2c-120">Если параметр <em>ObjectType</em> имеет значение <strong>АдпермобжпровидерспеЦифик</strong> , а <em>обжекттипеид</em> не предоставлено, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="3bf2c-120">An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bf2c-121"><strong>адпермобжтабле</strong></span><span class="sxs-lookup"><span data-stu-id="3bf2c-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="3bf2c-122">1,1</span><span class="sxs-lookup"><span data-stu-id="3bf2c-122">1</span></span></p></td>
<td><p><span data-ttu-id="3bf2c-123">Объект является таблицей.</span><span class="sxs-lookup"><span data-stu-id="3bf2c-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bf2c-124"><strong>адпермобжвиев</strong></span><span class="sxs-lookup"><span data-stu-id="3bf2c-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="3bf2c-125">5 </span><span class="sxs-lookup"><span data-stu-id="3bf2c-125">5</span></span></p></td>
<td><p><span data-ttu-id="3bf2c-126">Объект является представлением.</span><span class="sxs-lookup"><span data-stu-id="3bf2c-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

