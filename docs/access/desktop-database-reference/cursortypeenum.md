---
title: CursorTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c254c41bb066887e659c86a29ec4a91ca0de9cdd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482632"
---
# <a name="cursortypeenum"></a><span data-ttu-id="316af-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="316af-102">CursorTypeEnum</span></span>


<span data-ttu-id="316af-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="316af-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="316af-104">Указывает тип курсора, используемого в объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="316af-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="316af-105">Константа</span><span class="sxs-lookup"><span data-stu-id="316af-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="316af-106">Значение</span><span class="sxs-lookup"><span data-stu-id="316af-106">Value</span></span></p></th>
<th><p><span data-ttu-id="316af-107">Описание</span><span class="sxs-lookup"><span data-stu-id="316af-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="316af-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="316af-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="316af-109">2</span><span class="sxs-lookup"><span data-stu-id="316af-109">2</span></span></p></td>
<td><p><span data-ttu-id="316af-110">С помощью динамического курсора.</span><span class="sxs-lookup"><span data-stu-id="316af-110">Uses a dynamic cursor.</span></span> <span data-ttu-id="316af-111">Видны добавления, изменения и удаления другими пользователями, а все типы перемещения по <strong>набору записей</strong> , разрешены, за исключением закладки, если их не поддерживает поставщик.</span><span class="sxs-lookup"><span data-stu-id="316af-111">Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="316af-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="316af-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="316af-113">0</span><span class="sxs-lookup"><span data-stu-id="316af-113">0</span></span></p></td>
<td><p><span data-ttu-id="316af-114">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="316af-114">Default.</span></span> <span data-ttu-id="316af-115">Используется только для прямого курсора.</span><span class="sxs-lookup"><span data-stu-id="316af-115">Uses a forward-only cursor.</span></span> <span data-ttu-id="316af-116">Совпадает с статический курсор, за исключением того, что вы можно только просмотреть записей.</span><span class="sxs-lookup"><span data-stu-id="316af-116">Identical to a static cursor, except that you can only scroll forward through records.</span></span> <span data-ttu-id="316af-117">Это повышает производительность, если вам нужно сделать только один проход по <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="316af-117">This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="316af-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="316af-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="316af-119">1</span><span class="sxs-lookup"><span data-stu-id="316af-119">1</span></span></p></td>
<td><p><span data-ttu-id="316af-120">Использует курсор набора ключей.</span><span class="sxs-lookup"><span data-stu-id="316af-120">Uses a keyset cursor.</span></span> <span data-ttu-id="316af-121">Как динамический курсор, за исключением того, что нельзя просматривать записи, которые другие пользователи добавляют, несмотря на то, что записи, которые другие пользователи удалять недоступны из набора <strong>записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="316af-121">Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>.</span></span> <span data-ttu-id="316af-122">Изменения данных другие пользователи по-прежнему видимы.</span><span class="sxs-lookup"><span data-stu-id="316af-122">Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="316af-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="316af-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="316af-124">3</span><span class="sxs-lookup"><span data-stu-id="316af-124">3</span></span></p></td>
<td><p><span data-ttu-id="316af-125">Использует статический курсор.</span><span class="sxs-lookup"><span data-stu-id="316af-125">Uses a static cursor.</span></span> <span data-ttu-id="316af-126">Статические копия набора записей, которые можно использовать для поиска данных и создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="316af-126">A static copy of a set of records that you can use to find data or generate reports.</span></span> <span data-ttu-id="316af-127">Дополнения, изменения или удаления другие пользователи не отображаются.</span><span class="sxs-lookup"><span data-stu-id="316af-127">Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="316af-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="316af-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="316af-129">-1</span><span class="sxs-lookup"><span data-stu-id="316af-129">-1</span></span></p></td>
<td><p><span data-ttu-id="316af-130">Не указан тип курсора.</span><span class="sxs-lookup"><span data-stu-id="316af-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="316af-131">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="316af-131">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="316af-132">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="316af-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="316af-133">Constant</span><span class="sxs-lookup"><span data-stu-id="316af-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="316af-134">AdoEnums.CursorType.DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="316af-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="316af-135">AdoEnums.CursorType.FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="316af-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="316af-136">AdoEnums.CursorType.KEYSET</span><span class="sxs-lookup"><span data-stu-id="316af-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="316af-137">AdoEnums.CursorType.STATIC</span><span class="sxs-lookup"><span data-stu-id="316af-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="316af-138">AdoEnums.CursorType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="316af-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

