---
title: LockTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf882c6a63edbf3df067016a6ed793e05f41e74c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481366"
---
# <a name="locktypeenum"></a><span data-ttu-id="82732-102">LockTypeEnum</span><span class="sxs-lookup"><span data-stu-id="82732-102">LockTypeEnum</span></span>


<span data-ttu-id="82732-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="82732-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="82732-104">Указывает тип блокировки, помещенные на записей во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="82732-104">Specifies the type of lock placed on records during editing.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82732-105">Константа</span><span class="sxs-lookup"><span data-stu-id="82732-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="82732-106">Значение</span><span class="sxs-lookup"><span data-stu-id="82732-106">Value</span></span></p></th>
<th><p><span data-ttu-id="82732-107">Описание</span><span class="sxs-lookup"><span data-stu-id="82732-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82732-108"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="82732-108"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="82732-109">4</span><span class="sxs-lookup"><span data-stu-id="82732-109">4</span></span></p></td>
<td><p><span data-ttu-id="82732-110">Указывает оптимистичный пакета обновлений.</span><span class="sxs-lookup"><span data-stu-id="82732-110">Indicates optimistic batch updates.</span></span> <span data-ttu-id="82732-111">Требуется для пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="82732-111">Required for batch update mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82732-112"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="82732-112"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="82732-113">3</span><span class="sxs-lookup"><span data-stu-id="82732-113">3</span></span></p></td>
<td><p><span data-ttu-id="82732-114">Указывает, оптимистичный блокировки, записи по.</span><span class="sxs-lookup"><span data-stu-id="82732-114">Indicates optimistic locking, record by record.</span></span> <span data-ttu-id="82732-115">Поставщик использует оптимистичный блокировки блокировка записи только при вызове метода <a href="update-method-ado.md">Update</a> .</span><span class="sxs-lookup"><span data-stu-id="82732-115">The provider uses optimistic locking, locking records only when you call the <a href="update-method-ado.md">Update</a> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82732-116"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="82732-116"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="82732-117">2</span><span class="sxs-lookup"><span data-stu-id="82732-117">2</span></span></p></td>
<td><p><span data-ttu-id="82732-118">Указывает, жесткой блокировки, записи по.</span><span class="sxs-lookup"><span data-stu-id="82732-118">Indicates pessimistic locking, record by record.</span></span> <span data-ttu-id="82732-119">Поставщик выполняет, что является обязательным для обеспечения успешной редактирования записей, обычно путем блокировки сразу же после изменения записи в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="82732-119">The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately after editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82732-120"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="82732-120"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="82732-121">1</span><span class="sxs-lookup"><span data-stu-id="82732-121">1</span></span></p></td>
<td><p><span data-ttu-id="82732-122">Указывает записи только для чтения.</span><span class="sxs-lookup"><span data-stu-id="82732-122">Indicates read-only records.</span></span> <span data-ttu-id="82732-123">Невозможно изменить данные.</span><span class="sxs-lookup"><span data-stu-id="82732-123">You cannot alter the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82732-124"><strong>adLockUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="82732-124"><strong>adLockUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="82732-125">-1</span><span class="sxs-lookup"><span data-stu-id="82732-125">-1</span></span></p></td>
<td><p><span data-ttu-id="82732-126">Не указан тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="82732-126">Does not specify a type of lock.</span></span> <span data-ttu-id="82732-127">Для копирует копия создается с тем же типом блокировки, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="82732-127">For clones, the clone is created with the same lock type as the original.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="82732-128">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="82732-128">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="82732-129">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="82732-129">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82732-130">Constant</span><span class="sxs-lookup"><span data-stu-id="82732-130">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82732-131">AdoEnums.LockType.BATCHOPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="82732-131">AdoEnums.LockType.BATCHOPTIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82732-132">AdoEnums.LockType.OPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="82732-132">AdoEnums.LockType.OPTIMISTIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82732-133">AdoEnums.LockType.PESSIMISTIC</span><span class="sxs-lookup"><span data-stu-id="82732-133">AdoEnums.LockType.PESSIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82732-134">AdoEnums.LockType.READONLY</span><span class="sxs-lookup"><span data-stu-id="82732-134">AdoEnums.LockType.READONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82732-135">AdoEnums.LockType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="82732-135">AdoEnums.LockType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

