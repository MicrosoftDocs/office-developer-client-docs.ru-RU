---
title: LockTypeEnum (Справочник по базам данных Access на компьютере)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4b9dc49e647bdcd3123ade065da0c74538c9a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289866"
---
# <a name="locktypeenum"></a><span data-ttu-id="4d60e-102">LockTypeEnum</span><span class="sxs-lookup"><span data-stu-id="4d60e-102">LockTypeEnum</span></span>

<span data-ttu-id="4d60e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d60e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d60e-104">Указывает тип блокировки, помещаемой в записи во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="4d60e-104">Specifies the type of lock placed on records during editing.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d60e-105">Константа</span><span class="sxs-lookup"><span data-stu-id="4d60e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4d60e-106">Значение</span><span class="sxs-lookup"><span data-stu-id="4d60e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4d60e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4d60e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d60e-108"><strong>Адлоккбатчоптимистик</strong></span><span class="sxs-lookup"><span data-stu-id="4d60e-108"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="4d60e-109">SP4</span><span class="sxs-lookup"><span data-stu-id="4d60e-109">4</span></span></p></td>
<td><p><span data-ttu-id="4d60e-110">Указывает на неоптимистичные пакетные обновления.</span><span class="sxs-lookup"><span data-stu-id="4d60e-110">Indicates optimistic batch updates.</span></span> <span data-ttu-id="4d60e-111">Обязательный режим для режима пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="4d60e-111">Required for batch update mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d60e-112"><strong>Адлоккоптимистик</strong></span><span class="sxs-lookup"><span data-stu-id="4d60e-112"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="4d60e-113">4</span><span class="sxs-lookup"><span data-stu-id="4d60e-113">3</span></span></p></td>
<td><p><span data-ttu-id="4d60e-114">Указывает на оптимистичную блокировку, запись по записи.</span><span class="sxs-lookup"><span data-stu-id="4d60e-114">Indicates optimistic locking, record by record.</span></span> <span data-ttu-id="4d60e-115">Поставщик использует оптимистическую блокировку, блокируя записи только при вызове метода <a href="update-method-ado.md">Update</a> .</span><span class="sxs-lookup"><span data-stu-id="4d60e-115">The provider uses optimistic locking, locking records only when you call the <a href="update-method-ado.md">Update</a> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d60e-116"><strong>Адлоккпессимистик</strong></span><span class="sxs-lookup"><span data-stu-id="4d60e-116"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="4d60e-117">2</span><span class="sxs-lookup"><span data-stu-id="4d60e-117">2</span></span></p></td>
<td><p><span data-ttu-id="4d60e-118">Указывает на пессимистическую блокировку, запись по записи.</span><span class="sxs-lookup"><span data-stu-id="4d60e-118">Indicates pessimistic locking, record by record.</span></span> <span data-ttu-id="4d60e-119">Поставщик выполняет то, что необходимо для успешного редактирования записей, как правило, путем блокировки записей в источнике данных сразу же после редактирования.</span><span class="sxs-lookup"><span data-stu-id="4d60e-119">The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately after editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d60e-120"><strong>Адлоккреадонли</strong></span><span class="sxs-lookup"><span data-stu-id="4d60e-120"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="4d60e-121">1,1</span><span class="sxs-lookup"><span data-stu-id="4d60e-121">1</span></span></p></td>
<td><p><span data-ttu-id="4d60e-122">Указывает записи, предназначенные только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4d60e-122">Indicates read-only records.</span></span> <span data-ttu-id="4d60e-123">Вы не можете изменить данные.</span><span class="sxs-lookup"><span data-stu-id="4d60e-123">You cannot alter the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d60e-124"><strong>АдлоккунспеЦифиед</strong></span><span class="sxs-lookup"><span data-stu-id="4d60e-124"><strong>adLockUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="4d60e-125">–1</span><span class="sxs-lookup"><span data-stu-id="4d60e-125">-1</span></span></p></td>
<td><p><span data-ttu-id="4d60e-126">Не указывает тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="4d60e-126">Does not specify a type of lock.</span></span> <span data-ttu-id="4d60e-127">Для клонов создается клон с тем же типом блокировки, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="4d60e-127">For clones, the clone is created with the same lock type as the original.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4d60e-128">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="4d60e-128">ADO/WFC equivalent</span></span>

<span data-ttu-id="4d60e-129">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="4d60e-129">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d60e-130">Константа</span><span class="sxs-lookup"><span data-stu-id="4d60e-130">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d60e-131">Адоенумс. LockType. БАТЧОПТИМИСТИК</span><span class="sxs-lookup"><span data-stu-id="4d60e-131">AdoEnums.LockType.BATCHOPTIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d60e-132">Адоенумс. LockType. ОПТИМИСТИЧеская блокировка</span><span class="sxs-lookup"><span data-stu-id="4d60e-132">AdoEnums.LockType.OPTIMISTIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d60e-133">Адоенумс. LockType. ПЕССИМИСТическая блокировка</span><span class="sxs-lookup"><span data-stu-id="4d60e-133">AdoEnums.LockType.PESSIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d60e-134">Адоенумс. LockType. READONLY</span><span class="sxs-lookup"><span data-stu-id="4d60e-134">AdoEnums.LockType.READONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d60e-135">Адоенумс. LockType. unspecifieded</span><span class="sxs-lookup"><span data-stu-id="4d60e-135">AdoEnums.LockType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

