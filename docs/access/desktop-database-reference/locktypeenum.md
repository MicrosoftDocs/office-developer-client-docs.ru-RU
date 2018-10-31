---
title: LockTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 57cef1ca3a31665db1db517c22756213abf49042
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860534"
---
# <a name="locktypeenum"></a><span data-ttu-id="9a38d-102">LockTypeEnum</span><span class="sxs-lookup"><span data-stu-id="9a38d-102">LockTypeEnum</span></span>

<span data-ttu-id="9a38d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a38d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9a38d-104">Указывает тип блокировки, помещенные на записей во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="9a38d-104">Specifies the type of lock placed on records during editing.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a38d-105">Константа</span><span class="sxs-lookup"><span data-stu-id="9a38d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="9a38d-106">Значение</span><span class="sxs-lookup"><span data-stu-id="9a38d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9a38d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9a38d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-108"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-108"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-109">4</span><span class="sxs-lookup"><span data-stu-id="9a38d-109">4</span></span></p></td>
<td><p><span data-ttu-id="9a38d-110">Указывает оптимистичный пакета обновлений.</span><span class="sxs-lookup"><span data-stu-id="9a38d-110">Indicates optimistic batch updates.</span></span> <span data-ttu-id="9a38d-111">Требуется для пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="9a38d-111">Required for batch update mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38d-112"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-112"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-113">3</span><span class="sxs-lookup"><span data-stu-id="9a38d-113">3</span></span></p></td>
<td><p><span data-ttu-id="9a38d-114">Указывает, оптимистичный блокировки, записи по.</span><span class="sxs-lookup"><span data-stu-id="9a38d-114">Indicates optimistic locking, record by record.</span></span> <span data-ttu-id="9a38d-115">Поставщик использует оптимистичный блокировки блокировка записи только при вызове метода <a href="update-method-ado.md">Update</a> .</span><span class="sxs-lookup"><span data-stu-id="9a38d-115">The provider uses optimistic locking, locking records only when you call the <a href="update-method-ado.md">Update</a> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-116"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-116"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-117">2</span><span class="sxs-lookup"><span data-stu-id="9a38d-117">2</span></span></p></td>
<td><p><span data-ttu-id="9a38d-118">Указывает, жесткой блокировки, записи по.</span><span class="sxs-lookup"><span data-stu-id="9a38d-118">Indicates pessimistic locking, record by record.</span></span> <span data-ttu-id="9a38d-119">Поставщик выполняет, что является обязательным для обеспечения успешной редактирования записей, обычно путем блокировки сразу же после изменения записи в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="9a38d-119">The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately after editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38d-120"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-120"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-121">1</span><span class="sxs-lookup"><span data-stu-id="9a38d-121">1</span></span></p></td>
<td><p><span data-ttu-id="9a38d-122">Указывает записи только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9a38d-122">Indicates read-only records.</span></span> <span data-ttu-id="9a38d-123">Невозможно изменить данные.</span><span class="sxs-lookup"><span data-stu-id="9a38d-123">You cannot alter the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-124"><strong>adLockUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-124"><strong>adLockUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-125">-1</span><span class="sxs-lookup"><span data-stu-id="9a38d-125">-1</span></span></p></td>
<td><p><span data-ttu-id="9a38d-126">Не указан тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="9a38d-126">Does not specify a type of lock.</span></span> <span data-ttu-id="9a38d-127">Для копирует копия создается с тем же типом блокировки, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="9a38d-127">For clones, the clone is created with the same lock type as the original.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9a38d-128">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="9a38d-128">ADO/WFC equivalent</span></span>

<span data-ttu-id="9a38d-129">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9a38d-129">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a38d-130">Constant</span><span class="sxs-lookup"><span data-stu-id="9a38d-130">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-131">AdoEnums.LockType.BATCHOPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="9a38d-131">AdoEnums.LockType.BATCHOPTIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38d-132">AdoEnums.LockType.OPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="9a38d-132">AdoEnums.LockType.OPTIMISTIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-133">AdoEnums.LockType.PESSIMISTIC</span><span class="sxs-lookup"><span data-stu-id="9a38d-133">AdoEnums.LockType.PESSIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38d-134">AdoEnums.LockType.READONLY</span><span class="sxs-lookup"><span data-stu-id="9a38d-134">AdoEnums.LockType.READONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-135">AdoEnums.LockType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="9a38d-135">AdoEnums.LockType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

