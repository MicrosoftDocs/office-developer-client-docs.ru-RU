---
title: EventStatusEnum (Справочник по для настольных баз данных Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 027ecde525d603b15bb7844e99edc2534774bb37
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867617"
---
# <a name="eventstatusenum"></a><span data-ttu-id="0f8c7-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="0f8c7-102">EventStatusEnum</span></span>

<span data-ttu-id="0f8c7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f8c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f8c7-104">Указывает текущее состояние выполнения события.</span><span class="sxs-lookup"><span data-stu-id="0f8c7-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f8c7-105">Константа</span><span class="sxs-lookup"><span data-stu-id="0f8c7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0f8c7-106">Значение</span><span class="sxs-lookup"><span data-stu-id="0f8c7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0f8c7-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0f8c7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f8c7-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="0f8c7-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="0f8c7-109">4</span><span class="sxs-lookup"><span data-stu-id="0f8c7-109">4</span></span></p></td>
<td><p><span data-ttu-id="0f8c7-110">Отмена запросов на операцию, которая вызвала событие.</span><span class="sxs-lookup"><span data-stu-id="0f8c7-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f8c7-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="0f8c7-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="0f8c7-112">3</span><span class="sxs-lookup"><span data-stu-id="0f8c7-112">3</span></span></p></td>
<td><p><span data-ttu-id="0f8c7-113">Указывает, что операция не могут запрашивать отмену ожидающие операции.</span><span class="sxs-lookup"><span data-stu-id="0f8c7-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f8c7-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="0f8c7-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="0f8c7-115">2</span><span class="sxs-lookup"><span data-stu-id="0f8c7-115">2</span></span></p></td>
<td><p><span data-ttu-id="0f8c7-116">Указывает, что операция, которая вызвала событие сбой из-за ошибки или ошибки.</span><span class="sxs-lookup"><span data-stu-id="0f8c7-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f8c7-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="0f8c7-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="0f8c7-118">1</span><span class="sxs-lookup"><span data-stu-id="0f8c7-118">1</span></span></p></td>
<td><p><span data-ttu-id="0f8c7-119">Указывает, что операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="0f8c7-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f8c7-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="0f8c7-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="0f8c7-121">5</span><span class="sxs-lookup"><span data-stu-id="0f8c7-121">5</span></span></p></td>
<td><p><span data-ttu-id="0f8c7-122">До завершения выполнения метода события не позволяет последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="0f8c7-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0f8c7-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0f8c7-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="0f8c7-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0f8c7-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f8c7-125">Constant</span><span class="sxs-lookup"><span data-stu-id="0f8c7-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f8c7-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="0f8c7-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f8c7-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="0f8c7-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f8c7-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="0f8c7-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f8c7-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="0f8c7-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f8c7-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="0f8c7-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

