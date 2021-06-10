---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53e51f2386658ee975ec8847f7e5550ac22bbd8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281903"
---
# <a name="adcprop_asyncthreadpriority_enum"></a><span data-ttu-id="5d789-102">ADCPROP \_ ASYNCTHREADPRIORITY \_ ENUM</span><span class="sxs-lookup"><span data-stu-id="5d789-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="5d789-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d789-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d789-104">Для объекта RDS [Recordset](recordset-object-ado.md) указывается приоритет выполнения асинхронного потока, который извлекает данные.</span><span class="sxs-lookup"><span data-stu-id="5d789-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="5d789-105">Используйте эти константы с динамическим свойством **Recordset** **"Background Thread Priority",** которое ссылается в индексе динамического свойства ADO и задокументировано в документации [Microsoft Cursor Service для OLE DB.](microsoft-cursor-service-for-ole-db-ado-service-component.md)</span><span class="sxs-lookup"><span data-stu-id="5d789-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d789-106">Константа</span><span class="sxs-lookup"><span data-stu-id="5d789-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="5d789-107">Значение</span><span class="sxs-lookup"><span data-stu-id="5d789-107">Value</span></span></p></th>
<th><p><span data-ttu-id="5d789-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5d789-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d789-109"><strong>adPriorityAboveNormal</strong></span><span class="sxs-lookup"><span data-stu-id="5d789-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="5d789-110">4 </span><span class="sxs-lookup"><span data-stu-id="5d789-110">4</span></span></p></td>
<td><p><span data-ttu-id="5d789-111">Задает приоритет между обычным и самым высоким.</span><span class="sxs-lookup"><span data-stu-id="5d789-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d789-112"><strong>adPriorityBelowNormal</strong></span><span class="sxs-lookup"><span data-stu-id="5d789-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="5d789-113">2</span><span class="sxs-lookup"><span data-stu-id="5d789-113">2</span></span></p></td>
<td><p><span data-ttu-id="5d789-114">Задает приоритет между самым низким и нормальным.</span><span class="sxs-lookup"><span data-stu-id="5d789-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d789-115"><strong>adPriorityHighest</strong></span><span class="sxs-lookup"><span data-stu-id="5d789-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="5d789-116">5 </span><span class="sxs-lookup"><span data-stu-id="5d789-116">5</span></span></p></td>
<td><p><span data-ttu-id="5d789-117">Задает максимально возможный приоритет.</span><span class="sxs-lookup"><span data-stu-id="5d789-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d789-118"><strong>AdPriorityLowest</strong></span><span class="sxs-lookup"><span data-stu-id="5d789-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="5d789-119">1</span><span class="sxs-lookup"><span data-stu-id="5d789-119">1</span></span></p></td>
<td><p><span data-ttu-id="5d789-120">Задает приоритет до минимально возможного.</span><span class="sxs-lookup"><span data-stu-id="5d789-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d789-121"><strong>adPriorityNormal</strong></span><span class="sxs-lookup"><span data-stu-id="5d789-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="5d789-122">3</span><span class="sxs-lookup"><span data-stu-id="5d789-122">3</span></span></p></td>
<td><p><span data-ttu-id="5d789-123">Задает приоритет к нормальному.</span><span class="sxs-lookup"><span data-stu-id="5d789-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a><span data-ttu-id="5d789-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="5d789-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="5d789-125">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="5d789-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d789-126">Константа</span><span class="sxs-lookup"><span data-stu-id="5d789-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d789-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span><span class="sxs-lookup"><span data-stu-id="5d789-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d789-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span><span class="sxs-lookup"><span data-stu-id="5d789-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d789-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span><span class="sxs-lookup"><span data-stu-id="5d789-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d789-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span><span class="sxs-lookup"><span data-stu-id="5d789-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d789-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span><span class="sxs-lookup"><span data-stu-id="5d789-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

