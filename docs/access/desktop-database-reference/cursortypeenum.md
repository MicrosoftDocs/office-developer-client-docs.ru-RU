---
title: CursorTypeEnum (справочник по базам данных Access для настольных ПК)
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
# <a name="cursortypeenum"></a><span data-ttu-id="b2e6c-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="b2e6c-102">CursorTypeEnum</span></span>

<span data-ttu-id="b2e6c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2e6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2e6c-104">Указывает тип курсора, используемого в [объекте Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b2e6c-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2e6c-105">Константа</span><span class="sxs-lookup"><span data-stu-id="b2e6c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b2e6c-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b2e6c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b2e6c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b2e6c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2e6c-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="b2e6c-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="b2e6c-109">2 </span><span class="sxs-lookup"><span data-stu-id="b2e6c-109">2</span></span></p></td>
<td><p><span data-ttu-id="b2e6c-110">Использует динамический курсор.</span><span class="sxs-lookup"><span data-stu-id="b2e6c-110">Uses a dynamic cursor.</span></span> <span data-ttu-id="b2e6c-111">Добавления, изменения и удаления другими пользователями видны, и все типы перемещения через набор <strong>записей</strong> разрешены, за исключением закладок, если поставщик их не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="b2e6c-111">Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2e6c-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="b2e6c-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="b2e6c-113">0</span><span class="sxs-lookup"><span data-stu-id="b2e6c-113">0</span></span></p></td>
<td><p><span data-ttu-id="b2e6c-114">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2e6c-114">Default.</span></span> <span data-ttu-id="b2e6c-115">Использует курсор "только вперед".</span><span class="sxs-lookup"><span data-stu-id="b2e6c-115">Uses a forward-only cursor.</span></span> <span data-ttu-id="b2e6c-116">Идентично статическому курсору, за исключением того, что можно прокручивать только записи.</span><span class="sxs-lookup"><span data-stu-id="b2e6c-116">Identical to a static cursor, except that you can only scroll forward through records.</span></span> <span data-ttu-id="b2e6c-117">Это повышает производительность, если требуется сделать только один проход через <strong>набор записей.</strong></span><span class="sxs-lookup"><span data-stu-id="b2e6c-117">This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2e6c-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="b2e6c-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="b2e6c-119">1 </span><span class="sxs-lookup"><span data-stu-id="b2e6c-119">1</span></span></p></td>
<td><p><span data-ttu-id="b2e6c-120">Использует курсор наборов клавиш.</span><span class="sxs-lookup"><span data-stu-id="b2e6c-120">Uses a keyset cursor.</span></span> <span data-ttu-id="b2e6c-121">Как и динамический курсор, за исключением того, что вы не можете видеть записи, которые добавляют другие пользователи, хотя записи, удаляющиеся другими пользователями, недоступны из <strong>вашего recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="b2e6c-121">Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>.</span></span> <span data-ttu-id="b2e6c-122">Изменения данных другими пользователями по-прежнему видны.</span><span class="sxs-lookup"><span data-stu-id="b2e6c-122">Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2e6c-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="b2e6c-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="b2e6c-124">3 </span><span class="sxs-lookup"><span data-stu-id="b2e6c-124">3</span></span></p></td>
<td><p><span data-ttu-id="b2e6c-125">Использует статический курсор.</span><span class="sxs-lookup"><span data-stu-id="b2e6c-125">Uses a static cursor.</span></span> <span data-ttu-id="b2e6c-126">Статическая копия набора записей, которую можно использовать для поиска данных или создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="b2e6c-126">A static copy of a set of records that you can use to find data or generate reports.</span></span> <span data-ttu-id="b2e6c-127">Добавления, изменения или удаления другими пользователями не видны.</span><span class="sxs-lookup"><span data-stu-id="b2e6c-127">Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2e6c-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="b2e6c-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="b2e6c-129">–1</span><span class="sxs-lookup"><span data-stu-id="b2e6c-129">-1</span></span></p></td>
<td><p><span data-ttu-id="b2e6c-130">Не указывает тип курсора.</span><span class="sxs-lookup"><span data-stu-id="b2e6c-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b2e6c-131">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="b2e6c-131">ADO/WFC equivalent</span></span>

<span data-ttu-id="b2e6c-132">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b2e6c-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2e6c-133">Константа</span><span class="sxs-lookup"><span data-stu-id="b2e6c-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2e6c-134">AdoEnums.CursorType.DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="b2e6c-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2e6c-135">AdoEnums.CursorType.FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="b2e6c-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2e6c-136">AdoEnums.CursorType.KEYSET</span><span class="sxs-lookup"><span data-stu-id="b2e6c-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2e6c-137">AdoEnums.CursorType.STATIC</span><span class="sxs-lookup"><span data-stu-id="b2e6c-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2e6c-138">AdoEnums.CursorType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="b2e6c-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

