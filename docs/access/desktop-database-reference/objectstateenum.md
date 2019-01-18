---
title: ObjectStateEnum (Справочник по для настольных баз данных Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712269"
---
# <a name="objectstateenum"></a><span data-ttu-id="1d802-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="1d802-102">ObjectStateEnum</span></span>

<span data-ttu-id="1d802-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d802-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d802-104">Указывает, является ли объект открытой или закрытой, подключение к источнику данных, выполнение команды или получения данных.</span><span class="sxs-lookup"><span data-stu-id="1d802-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d802-105">Константа</span><span class="sxs-lookup"><span data-stu-id="1d802-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1d802-106">Значение</span><span class="sxs-lookup"><span data-stu-id="1d802-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1d802-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1d802-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d802-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="1d802-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="1d802-109">0</span><span class="sxs-lookup"><span data-stu-id="1d802-109">0</span></span></p></td>
<td><p><span data-ttu-id="1d802-110">Указывает, что объект закрыт.</span><span class="sxs-lookup"><span data-stu-id="1d802-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d802-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="1d802-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="1d802-112">1</span><span class="sxs-lookup"><span data-stu-id="1d802-112">1</span></span></p></td>
<td><p><span data-ttu-id="1d802-113">Указывает, что объект открыт.</span><span class="sxs-lookup"><span data-stu-id="1d802-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d802-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="1d802-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="1d802-115">2</span><span class="sxs-lookup"><span data-stu-id="1d802-115">2</span></span></p></td>
<td><p><span data-ttu-id="1d802-116">Указывает, что объект подключения.</span><span class="sxs-lookup"><span data-stu-id="1d802-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d802-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="1d802-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="1d802-118">4</span><span class="sxs-lookup"><span data-stu-id="1d802-118">4</span></span></p></td>
<td><p><span data-ttu-id="1d802-119">Указывает, что объект выполняет команду.</span><span class="sxs-lookup"><span data-stu-id="1d802-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d802-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="1d802-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="1d802-121">8</span><span class="sxs-lookup"><span data-stu-id="1d802-121">8</span></span></p></td>
<td><p><span data-ttu-id="1d802-122">Указывает, извлекается строк объекта.</span><span class="sxs-lookup"><span data-stu-id="1d802-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1d802-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1d802-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="1d802-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1d802-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d802-125">Константа</span><span class="sxs-lookup"><span data-stu-id="1d802-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d802-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="1d802-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d802-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="1d802-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d802-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="1d802-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d802-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="1d802-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d802-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="1d802-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

