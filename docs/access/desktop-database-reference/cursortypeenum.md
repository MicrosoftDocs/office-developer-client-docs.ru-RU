---
title: Курсортипинум (Справочник по базам данных Access на компьютере)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295165"
---
# <a name="cursortypeenum"></a><span data-ttu-id="118c1-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="118c1-102">CursorTypeEnum</span></span>

<span data-ttu-id="118c1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="118c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="118c1-104">Указывает тип курсора, используемого в объекте [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="118c1-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="118c1-105">Константа</span><span class="sxs-lookup"><span data-stu-id="118c1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="118c1-106">Значение</span><span class="sxs-lookup"><span data-stu-id="118c1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="118c1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="118c1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="118c1-108"><strong>Адопендинамик</strong></span><span class="sxs-lookup"><span data-stu-id="118c1-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="118c1-109">2</span><span class="sxs-lookup"><span data-stu-id="118c1-109">2</span></span></p></td>
<td><p><span data-ttu-id="118c1-110">Использование динамического курсора.</span><span class="sxs-lookup"><span data-stu-id="118c1-110">Uses a dynamic cursor.</span></span> <span data-ttu-id="118c1-111">Для других пользователей отображаются дополнения, изменения и удаления, а также все типы передвижений по <strong>набору записей</strong> , кроме закладок, если они не поддерживаются поставщиком.</span><span class="sxs-lookup"><span data-stu-id="118c1-111">Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="118c1-112"><strong>Адопенфорвардонли</strong></span><span class="sxs-lookup"><span data-stu-id="118c1-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="118c1-113">нуль</span><span class="sxs-lookup"><span data-stu-id="118c1-113">0</span></span></p></td>
<td><p><span data-ttu-id="118c1-114">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="118c1-114">Default.</span></span> <span data-ttu-id="118c1-115">Использует однонаправленный курсор.</span><span class="sxs-lookup"><span data-stu-id="118c1-115">Uses a forward-only cursor.</span></span> <span data-ttu-id="118c1-116">Идентично статическому курсору, за исключением того, что можно прокручивать только записи вперед.</span><span class="sxs-lookup"><span data-stu-id="118c1-116">Identical to a static cursor, except that you can only scroll forward through records.</span></span> <span data-ttu-id="118c1-117">Это повышает производительность, если необходимо выполнить только один проход через <strong>набор записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="118c1-117">This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="118c1-118"><strong>Адопенкэйсет</strong></span><span class="sxs-lookup"><span data-stu-id="118c1-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="118c1-119">1,1</span><span class="sxs-lookup"><span data-stu-id="118c1-119">1</span></span></p></td>
<td><p><span data-ttu-id="118c1-120">Использует курсор KEYSET.</span><span class="sxs-lookup"><span data-stu-id="118c1-120">Uses a keyset cursor.</span></span> <span data-ttu-id="118c1-121">Как и динамический курсор, за исключением того, что записи, добавленные другими пользователями, не видны, хотя записи, которые другие пользователи удаляют, недоступны из <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="118c1-121">Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>.</span></span> <span data-ttu-id="118c1-122">Изменения данных, внесенные другими пользователями, по-прежнему видимы.</span><span class="sxs-lookup"><span data-stu-id="118c1-122">Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="118c1-123"><strong>Адопенстатик</strong></span><span class="sxs-lookup"><span data-stu-id="118c1-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="118c1-124">4</span><span class="sxs-lookup"><span data-stu-id="118c1-124">3</span></span></p></td>
<td><p><span data-ttu-id="118c1-125">Использует статический курсор.</span><span class="sxs-lookup"><span data-stu-id="118c1-125">Uses a static cursor.</span></span> <span data-ttu-id="118c1-126">Статическая копия набора записей, которую можно использовать для поиска данных или создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="118c1-126">A static copy of a set of records that you can use to find data or generate reports.</span></span> <span data-ttu-id="118c1-127">Добавленные, измененные или удаленные пользователи не отображаются.</span><span class="sxs-lookup"><span data-stu-id="118c1-127">Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="118c1-128"><strong>АдопенунспеЦифиед</strong></span><span class="sxs-lookup"><span data-stu-id="118c1-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="118c1-129">–1</span><span class="sxs-lookup"><span data-stu-id="118c1-129">-1</span></span></p></td>
<td><p><span data-ttu-id="118c1-130">Не указывает тип курсора.</span><span class="sxs-lookup"><span data-stu-id="118c1-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="118c1-131">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="118c1-131">ADO/WFC equivalent</span></span>

<span data-ttu-id="118c1-132">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="118c1-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="118c1-133">Константа</span><span class="sxs-lookup"><span data-stu-id="118c1-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="118c1-134">Адоенумс. CursorType. DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="118c1-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="118c1-135">Адоенумс. CursorType. ФОРВАРДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="118c1-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="118c1-136">Адоенумс. CursorType. KEYSET</span><span class="sxs-lookup"><span data-stu-id="118c1-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="118c1-137">Адоенумс. CursorType. STATIC</span><span class="sxs-lookup"><span data-stu-id="118c1-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="118c1-138">Адоенумс. CursorType. unspecifieded</span><span class="sxs-lookup"><span data-stu-id="118c1-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

