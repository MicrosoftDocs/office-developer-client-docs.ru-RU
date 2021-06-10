---
title: CursorTypeEnum (Ссылка на настольные базы данных)
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
# <a name="cursortypeenum"></a><span data-ttu-id="3cc4b-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="3cc4b-102">CursorTypeEnum</span></span>

<span data-ttu-id="3cc4b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cc4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cc4b-104">Указывает тип курсора, используемого в [объекте Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="3cc4b-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cc4b-105">Константа</span><span class="sxs-lookup"><span data-stu-id="3cc4b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3cc4b-106">Значение</span><span class="sxs-lookup"><span data-stu-id="3cc4b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3cc4b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3cc4b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cc4b-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="3cc4b-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc4b-109">2</span><span class="sxs-lookup"><span data-stu-id="3cc4b-109">2</span></span></p></td>
<td><p><span data-ttu-id="3cc4b-110">Использует динамический курсор.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-110">Uses a dynamic cursor.</span></span> <span data-ttu-id="3cc4b-111">Видны добавления, изменения и удаления других пользователей, а также разрешены все типы перемещения через <strong>Набор</strong> записей, за исключением закладок, если поставщик не поддерживает их.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-111">Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc4b-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="3cc4b-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc4b-113">0</span><span class="sxs-lookup"><span data-stu-id="3cc4b-113">0</span></span></p></td>
<td><p><span data-ttu-id="3cc4b-114">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-114">Default.</span></span> <span data-ttu-id="3cc4b-115">Использует курсор только для нападающих.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-115">Uses a forward-only cursor.</span></span> <span data-ttu-id="3cc4b-116">Идентично статическому курсору, за исключением того, что можно прокручивать только записи.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-116">Identical to a static cursor, except that you can only scroll forward through records.</span></span> <span data-ttu-id="3cc4b-117">Это повышает производительность, если требуется сделать только один проход через <strong>набор Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="3cc4b-117">This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc4b-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="3cc4b-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc4b-119">1</span><span class="sxs-lookup"><span data-stu-id="3cc4b-119">1</span></span></p></td>
<td><p><span data-ttu-id="3cc4b-120">Использует курсор наборов ключей.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-120">Uses a keyset cursor.</span></span> <span data-ttu-id="3cc4b-121">Как динамический курсор, за исключением того, что вы не можете видеть записи, которые добавляют другие пользователи, хотя записи, которые другие пользователи удаляют, недоступны из <strong>вашего Набор записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-121">Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>.</span></span> <span data-ttu-id="3cc4b-122">Изменения данных другими пользователями по-прежнему видны.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-122">Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc4b-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="3cc4b-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc4b-124">3</span><span class="sxs-lookup"><span data-stu-id="3cc4b-124">3</span></span></p></td>
<td><p><span data-ttu-id="3cc4b-125">Использует статический курсор.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-125">Uses a static cursor.</span></span> <span data-ttu-id="3cc4b-126">Статическая копия набора записей, которые можно использовать для поиска данных или создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-126">A static copy of a set of records that you can use to find data or generate reports.</span></span> <span data-ttu-id="3cc4b-127">Добавления, изменения или удаления других пользователей не видны.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-127">Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc4b-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="3cc4b-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc4b-129">–1</span><span class="sxs-lookup"><span data-stu-id="3cc4b-129">-1</span></span></p></td>
<td><p><span data-ttu-id="3cc4b-130">Не указывает тип курсора.</span><span class="sxs-lookup"><span data-stu-id="3cc4b-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="3cc4b-131">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="3cc4b-131">ADO/WFC equivalent</span></span>

<span data-ttu-id="3cc4b-132">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="3cc4b-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cc4b-133">Константа</span><span class="sxs-lookup"><span data-stu-id="3cc4b-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cc4b-134">AdoEnums.CursorType.DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="3cc4b-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc4b-135">AdoEnums.CursorType.FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="3cc4b-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc4b-136">AdoEnums.CursorType.KEYSET</span><span class="sxs-lookup"><span data-stu-id="3cc4b-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc4b-137">AdoEnums.CursorType.STATIC</span><span class="sxs-lookup"><span data-stu-id="3cc4b-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc4b-138">AdoEnums.CursorType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="3cc4b-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

