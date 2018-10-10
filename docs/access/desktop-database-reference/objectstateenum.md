---
title: ObjectStateEnum (Справочник по для настольных баз данных Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a08713e5363cb023021e2dd5acb6b38431a6b5e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483103"
---
# <a name="objectstateenum"></a><span data-ttu-id="c318c-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="c318c-102">ObjectStateEnum</span></span>


<span data-ttu-id="c318c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c318c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c318c-104">Указывает, является ли объект открытой или закрытой, подключение к источнику данных, выполнение команды или получения данных.</span><span class="sxs-lookup"><span data-stu-id="c318c-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c318c-105">Константа</span><span class="sxs-lookup"><span data-stu-id="c318c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c318c-106">Значение</span><span class="sxs-lookup"><span data-stu-id="c318c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c318c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c318c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c318c-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="c318c-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="c318c-109">0</span><span class="sxs-lookup"><span data-stu-id="c318c-109">0</span></span></p></td>
<td><p><span data-ttu-id="c318c-110">Указывает, что объект закрыт.</span><span class="sxs-lookup"><span data-stu-id="c318c-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c318c-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="c318c-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="c318c-112">1</span><span class="sxs-lookup"><span data-stu-id="c318c-112">1</span></span></p></td>
<td><p><span data-ttu-id="c318c-113">Указывает, что объект открыт.</span><span class="sxs-lookup"><span data-stu-id="c318c-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c318c-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="c318c-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="c318c-115">2</span><span class="sxs-lookup"><span data-stu-id="c318c-115">2</span></span></p></td>
<td><p><span data-ttu-id="c318c-116">Указывает, что объект подключения.</span><span class="sxs-lookup"><span data-stu-id="c318c-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c318c-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="c318c-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="c318c-118">4</span><span class="sxs-lookup"><span data-stu-id="c318c-118">4</span></span></p></td>
<td><p><span data-ttu-id="c318c-119">Указывает, что объект выполняет команду.</span><span class="sxs-lookup"><span data-stu-id="c318c-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c318c-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="c318c-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="c318c-121">8</span><span class="sxs-lookup"><span data-stu-id="c318c-121">8</span></span></p></td>
<td><p><span data-ttu-id="c318c-122">Указывает, извлекается строк объекта.</span><span class="sxs-lookup"><span data-stu-id="c318c-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c318c-123">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="c318c-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="c318c-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c318c-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c318c-125">Constant</span><span class="sxs-lookup"><span data-stu-id="c318c-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c318c-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="c318c-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c318c-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="c318c-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c318c-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="c318c-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c318c-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="c318c-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c318c-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="c318c-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

