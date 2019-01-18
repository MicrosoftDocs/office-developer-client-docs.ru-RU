---
title: EventStatusEnum (Справочник по для настольных баз данных Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712584"
---
# <a name="eventstatusenum"></a><span data-ttu-id="0feca-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="0feca-102">EventStatusEnum</span></span>

<span data-ttu-id="0feca-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0feca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0feca-104">Указывает текущее состояние выполнения события.</span><span class="sxs-lookup"><span data-stu-id="0feca-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0feca-105">Константа</span><span class="sxs-lookup"><span data-stu-id="0feca-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0feca-106">Значение</span><span class="sxs-lookup"><span data-stu-id="0feca-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0feca-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0feca-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0feca-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="0feca-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="0feca-109">4</span><span class="sxs-lookup"><span data-stu-id="0feca-109">4</span></span></p></td>
<td><p><span data-ttu-id="0feca-110">Отмена запросов на операцию, которая вызвала событие.</span><span class="sxs-lookup"><span data-stu-id="0feca-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0feca-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="0feca-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="0feca-112">3</span><span class="sxs-lookup"><span data-stu-id="0feca-112">3</span></span></p></td>
<td><p><span data-ttu-id="0feca-113">Указывает, что операция не могут запрашивать отмену ожидающие операции.</span><span class="sxs-lookup"><span data-stu-id="0feca-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0feca-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="0feca-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="0feca-115">2</span><span class="sxs-lookup"><span data-stu-id="0feca-115">2</span></span></p></td>
<td><p><span data-ttu-id="0feca-116">Указывает, что операция, которая вызвала событие сбой из-за ошибки или ошибки.</span><span class="sxs-lookup"><span data-stu-id="0feca-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0feca-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="0feca-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="0feca-118">1</span><span class="sxs-lookup"><span data-stu-id="0feca-118">1</span></span></p></td>
<td><p><span data-ttu-id="0feca-119">Указывает, что операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="0feca-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0feca-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="0feca-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="0feca-121">5</span><span class="sxs-lookup"><span data-stu-id="0feca-121">5</span></span></p></td>
<td><p><span data-ttu-id="0feca-122">До завершения выполнения метода события не позволяет последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="0feca-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0feca-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0feca-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="0feca-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0feca-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0feca-125">Константа</span><span class="sxs-lookup"><span data-stu-id="0feca-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0feca-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="0feca-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0feca-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="0feca-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0feca-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="0feca-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0feca-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="0feca-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0feca-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="0feca-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

