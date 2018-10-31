---
title: CursorTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c394f8000f1d4ae7867d83974e0e186616145fb5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864030"
---
# <a name="cursortypeenum"></a><span data-ttu-id="ade3c-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="ade3c-102">CursorTypeEnum</span></span>

<span data-ttu-id="ade3c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ade3c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ade3c-104">Указывает тип курсора, используемого в объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ade3c-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ade3c-105">Константа</span><span class="sxs-lookup"><span data-stu-id="ade3c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ade3c-106">Значение</span><span class="sxs-lookup"><span data-stu-id="ade3c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ade3c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ade3c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ade3c-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="ade3c-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="ade3c-109">2</span><span class="sxs-lookup"><span data-stu-id="ade3c-109">2</span></span></p></td>
<td><p><span data-ttu-id="ade3c-110">С помощью динамического курсора.</span><span class="sxs-lookup"><span data-stu-id="ade3c-110">Uses a dynamic cursor.</span></span> <span data-ttu-id="ade3c-111">Видны добавления, изменения и удаления другими пользователями, а все типы перемещения по <strong>набору записей</strong> , разрешены, за исключением закладки, если их не поддерживает поставщик.</span><span class="sxs-lookup"><span data-stu-id="ade3c-111">Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ade3c-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="ade3c-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="ade3c-113">0</span><span class="sxs-lookup"><span data-stu-id="ade3c-113">0</span></span></p></td>
<td><p><span data-ttu-id="ade3c-114">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ade3c-114">Default.</span></span> <span data-ttu-id="ade3c-115">Используется только для прямого курсора.</span><span class="sxs-lookup"><span data-stu-id="ade3c-115">Uses a forward-only cursor.</span></span> <span data-ttu-id="ade3c-116">Совпадает с статический курсор, за исключением того, что вы можно только просмотреть записей.</span><span class="sxs-lookup"><span data-stu-id="ade3c-116">Identical to a static cursor, except that you can only scroll forward through records.</span></span> <span data-ttu-id="ade3c-117">Это повышает производительность, если вам нужно сделать только один проход по <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="ade3c-117">This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ade3c-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="ade3c-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="ade3c-119">1</span><span class="sxs-lookup"><span data-stu-id="ade3c-119">1</span></span></p></td>
<td><p><span data-ttu-id="ade3c-120">Использует курсор набора ключей.</span><span class="sxs-lookup"><span data-stu-id="ade3c-120">Uses a keyset cursor.</span></span> <span data-ttu-id="ade3c-121">Как динамический курсор, за исключением того, что нельзя просматривать записи, которые другие пользователи добавляют, несмотря на то, что записи, которые другие пользователи удалять недоступны из набора <strong>записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="ade3c-121">Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>.</span></span> <span data-ttu-id="ade3c-122">Изменения данных другие пользователи по-прежнему видимы.</span><span class="sxs-lookup"><span data-stu-id="ade3c-122">Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ade3c-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="ade3c-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="ade3c-124">3</span><span class="sxs-lookup"><span data-stu-id="ade3c-124">3</span></span></p></td>
<td><p><span data-ttu-id="ade3c-125">Использует статический курсор.</span><span class="sxs-lookup"><span data-stu-id="ade3c-125">Uses a static cursor.</span></span> <span data-ttu-id="ade3c-126">Статические копия набора записей, которые можно использовать для поиска данных и создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="ade3c-126">A static copy of a set of records that you can use to find data or generate reports.</span></span> <span data-ttu-id="ade3c-127">Дополнения, изменения или удаления другие пользователи не отображаются.</span><span class="sxs-lookup"><span data-stu-id="ade3c-127">Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ade3c-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="ade3c-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="ade3c-129">-1</span><span class="sxs-lookup"><span data-stu-id="ade3c-129">-1</span></span></p></td>
<td><p><span data-ttu-id="ade3c-130">Не указан тип курсора.</span><span class="sxs-lookup"><span data-stu-id="ade3c-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ade3c-131">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ade3c-131">ADO/WFC equivalent</span></span>

<span data-ttu-id="ade3c-132">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ade3c-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ade3c-133">Constant</span><span class="sxs-lookup"><span data-stu-id="ade3c-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ade3c-134">AdoEnums.CursorType.DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="ade3c-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ade3c-135">AdoEnums.CursorType.FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="ade3c-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ade3c-136">AdoEnums.CursorType.KEYSET</span><span class="sxs-lookup"><span data-stu-id="ade3c-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ade3c-137">AdoEnums.CursorType.STATIC</span><span class="sxs-lookup"><span data-stu-id="ade3c-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ade3c-138">AdoEnums.CursorType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="ade3c-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

