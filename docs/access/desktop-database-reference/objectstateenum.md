---
title: Обжектстатинум (Справочник по базам данных Access на компьютере)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288527"
---
# <a name="objectstateenum"></a><span data-ttu-id="d2d4d-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="d2d4d-102">ObjectStateEnum</span></span>

<span data-ttu-id="d2d4d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2d4d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2d4d-104">Указывает, является ли объект открытым или закрытым, подключается к источнику данных, выполняя команду или получая данные.</span><span class="sxs-lookup"><span data-stu-id="d2d4d-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2d4d-105">Константа</span><span class="sxs-lookup"><span data-stu-id="d2d4d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d2d4d-106">Значение</span><span class="sxs-lookup"><span data-stu-id="d2d4d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d2d4d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d2d4d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2d4d-108"><strong>адстатеклосед</strong></span><span class="sxs-lookup"><span data-stu-id="d2d4d-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="d2d4d-109">нуль</span><span class="sxs-lookup"><span data-stu-id="d2d4d-109">0</span></span></p></td>
<td><p><span data-ttu-id="d2d4d-110">Указывает, что объект закрыт.</span><span class="sxs-lookup"><span data-stu-id="d2d4d-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2d4d-111"><strong>адстатеопен</strong></span><span class="sxs-lookup"><span data-stu-id="d2d4d-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="d2d4d-112">1,1</span><span class="sxs-lookup"><span data-stu-id="d2d4d-112">1</span></span></p></td>
<td><p><span data-ttu-id="d2d4d-113">Указывает, что объект открыт.</span><span class="sxs-lookup"><span data-stu-id="d2d4d-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2d4d-114"><strong>адстатеконнектинг</strong></span><span class="sxs-lookup"><span data-stu-id="d2d4d-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="d2d4d-115">2</span><span class="sxs-lookup"><span data-stu-id="d2d4d-115">2</span></span></p></td>
<td><p><span data-ttu-id="d2d4d-116">Указывает, что объект подключается.</span><span class="sxs-lookup"><span data-stu-id="d2d4d-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2d4d-117"><strong>адстатиксекутинг</strong></span><span class="sxs-lookup"><span data-stu-id="d2d4d-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="d2d4d-118">4 </span><span class="sxs-lookup"><span data-stu-id="d2d4d-118">4</span></span></p></td>
<td><p><span data-ttu-id="d2d4d-119">Указывает, что объект выполняет команду.</span><span class="sxs-lookup"><span data-stu-id="d2d4d-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2d4d-120"><strong>адстатефетчинг</strong></span><span class="sxs-lookup"><span data-stu-id="d2d4d-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="d2d4d-121">8 </span><span class="sxs-lookup"><span data-stu-id="d2d4d-121">8</span></span></p></td>
<td><p><span data-ttu-id="d2d4d-122">Указывает, что извлекаются строки объекта.</span><span class="sxs-lookup"><span data-stu-id="d2d4d-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d2d4d-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d2d4d-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="d2d4d-124">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="d2d4d-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2d4d-125">Константа</span><span class="sxs-lookup"><span data-stu-id="d2d4d-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2d4d-126">Адоенумс. Обжектстате. CLOSED</span><span class="sxs-lookup"><span data-stu-id="d2d4d-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2d4d-127">Адоенумс. Обжектстате. OPEN</span><span class="sxs-lookup"><span data-stu-id="d2d4d-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2d4d-128">Адоенумс. Обжектстате. подключение</span><span class="sxs-lookup"><span data-stu-id="d2d4d-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2d4d-129">Адоенумс. Обжектстате. выполнение</span><span class="sxs-lookup"><span data-stu-id="d2d4d-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2d4d-130">Адоенумс. Обжектстате. получение</span><span class="sxs-lookup"><span data-stu-id="d2d4d-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

