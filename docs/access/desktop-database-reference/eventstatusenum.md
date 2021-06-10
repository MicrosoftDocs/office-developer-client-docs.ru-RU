---
title: EventStatusEnum (Ссылка на настольные базы данных)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293275"
---
# <a name="eventstatusenum"></a><span data-ttu-id="47b3b-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="47b3b-102">EventStatusEnum</span></span>

<span data-ttu-id="47b3b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47b3b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47b3b-104">Указывает текущее состояние выполнения события.</span><span class="sxs-lookup"><span data-stu-id="47b3b-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47b3b-105">Константа</span><span class="sxs-lookup"><span data-stu-id="47b3b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="47b3b-106">Значение</span><span class="sxs-lookup"><span data-stu-id="47b3b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="47b3b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="47b3b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47b3b-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="47b3b-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="47b3b-109">4 </span><span class="sxs-lookup"><span data-stu-id="47b3b-109">4</span></span></p></td>
<td><p><span data-ttu-id="47b3b-110">Запрашивает отмену операции, из-за чего произошло событие.</span><span class="sxs-lookup"><span data-stu-id="47b3b-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b3b-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="47b3b-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="47b3b-112">3</span><span class="sxs-lookup"><span data-stu-id="47b3b-112">3</span></span></p></td>
<td><p><span data-ttu-id="47b3b-113">Указывает, что операция не может запрашивать отмену ожидаемой операции.</span><span class="sxs-lookup"><span data-stu-id="47b3b-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b3b-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="47b3b-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="47b3b-115">2</span><span class="sxs-lookup"><span data-stu-id="47b3b-115">2</span></span></p></td>
<td><p><span data-ttu-id="47b3b-116">Указывает, что операция, вызвавла сбой события из-за ошибки или ошибок.</span><span class="sxs-lookup"><span data-stu-id="47b3b-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b3b-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="47b3b-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="47b3b-118">1</span><span class="sxs-lookup"><span data-stu-id="47b3b-118">1</span></span></p></td>
<td><p><span data-ttu-id="47b3b-119">Указывает, что операция, которая стала причиной события, была успешной.</span><span class="sxs-lookup"><span data-stu-id="47b3b-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b3b-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="47b3b-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="47b3b-121">5 </span><span class="sxs-lookup"><span data-stu-id="47b3b-121">5</span></span></p></td>
<td><p><span data-ttu-id="47b3b-122">Предотвращает последующие уведомления до завершения выполнения метода события.</span><span class="sxs-lookup"><span data-stu-id="47b3b-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="47b3b-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="47b3b-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="47b3b-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="47b3b-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47b3b-125">Константа</span><span class="sxs-lookup"><span data-stu-id="47b3b-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47b3b-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="47b3b-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b3b-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="47b3b-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b3b-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="47b3b-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b3b-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="47b3b-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b3b-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="47b3b-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

