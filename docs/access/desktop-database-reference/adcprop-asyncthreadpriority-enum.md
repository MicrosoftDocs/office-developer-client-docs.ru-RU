---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: ef191813e72ade80a7944f09d76f27c2b2f2738c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874925"
---
# <a name="adcpropasyncthreadpriorityenum"></a><span data-ttu-id="537d6-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span><span class="sxs-lookup"><span data-stu-id="537d6-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="537d6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="537d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="537d6-104">Объект служб удаленных рабочих СТОЛОВ [записей](recordset-object-ado.md) указывает приоритет выполнения асинхронного потока, который получает данные.</span><span class="sxs-lookup"><span data-stu-id="537d6-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="537d6-105">Используйте эти константы с свойство динамических «**Приоритет потока фона**» **набора записей** , которое по ссылке в индексе динамические свойства ADO и описаны в документации по [Microsoft служба курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) .</span><span class="sxs-lookup"><span data-stu-id="537d6-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="537d6-106">Константа</span><span class="sxs-lookup"><span data-stu-id="537d6-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="537d6-107">Значение</span><span class="sxs-lookup"><span data-stu-id="537d6-107">Value</span></span></p></th>
<th><p><span data-ttu-id="537d6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="537d6-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="537d6-109"><strong>adPriorityAboveNormal</strong></span><span class="sxs-lookup"><span data-stu-id="537d6-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="537d6-110">4</span><span class="sxs-lookup"><span data-stu-id="537d6-110">4</span></span></p></td>
<td><p><span data-ttu-id="537d6-111">Задает между обычной и самый высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="537d6-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537d6-112"><strong>adPriorityBelowNormal</strong></span><span class="sxs-lookup"><span data-stu-id="537d6-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="537d6-113">2</span><span class="sxs-lookup"><span data-stu-id="537d6-113">2</span></span></p></td>
<td><p><span data-ttu-id="537d6-114">Задает приоритет между низкий и обычный.</span><span class="sxs-lookup"><span data-stu-id="537d6-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537d6-115"><strong>adPriorityHighest</strong></span><span class="sxs-lookup"><span data-stu-id="537d6-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="537d6-116">5</span><span class="sxs-lookup"><span data-stu-id="537d6-116">5</span></span></p></td>
<td><p><span data-ttu-id="537d6-117">Задает приоритет к наибольшим возможной.</span><span class="sxs-lookup"><span data-stu-id="537d6-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537d6-118"><strong>AdPriorityLowest</strong></span><span class="sxs-lookup"><span data-stu-id="537d6-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="537d6-119">1</span><span class="sxs-lookup"><span data-stu-id="537d6-119">1</span></span></p></td>
<td><p><span data-ttu-id="537d6-120">Задает приоритет до наименьшего возможного.</span><span class="sxs-lookup"><span data-stu-id="537d6-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537d6-121"><strong>adPriorityNormal</strong></span><span class="sxs-lookup"><span data-stu-id="537d6-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="537d6-122">3</span><span class="sxs-lookup"><span data-stu-id="537d6-122">3</span></span></p></td>
<td><p><span data-ttu-id="537d6-123">Задает приоритет normal.</span><span class="sxs-lookup"><span data-stu-id="537d6-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a><span data-ttu-id="537d6-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="537d6-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="537d6-125">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="537d6-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="537d6-126">Constant</span><span class="sxs-lookup"><span data-stu-id="537d6-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="537d6-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span><span class="sxs-lookup"><span data-stu-id="537d6-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537d6-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span><span class="sxs-lookup"><span data-stu-id="537d6-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537d6-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span><span class="sxs-lookup"><span data-stu-id="537d6-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537d6-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span><span class="sxs-lookup"><span data-stu-id="537d6-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537d6-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span><span class="sxs-lookup"><span data-stu-id="537d6-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

