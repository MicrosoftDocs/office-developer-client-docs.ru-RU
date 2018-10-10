---
title: EventStatusEnum (Справочник по для настольных баз данных Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f49f584603c25997e1b01b94f23aaf9f5429a9e4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479751"
---
# <a name="eventstatusenum"></a><span data-ttu-id="77665-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="77665-102">EventStatusEnum</span></span>


<span data-ttu-id="77665-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="77665-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="77665-104">Указывает текущее состояние выполнения события.</span><span class="sxs-lookup"><span data-stu-id="77665-104">Specifies the current status of the execution of an event.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77665-105">Константа</span><span class="sxs-lookup"><span data-stu-id="77665-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="77665-106">Значение</span><span class="sxs-lookup"><span data-stu-id="77665-106">Value</span></span></p></th>
<th><p><span data-ttu-id="77665-107">Описание</span><span class="sxs-lookup"><span data-stu-id="77665-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77665-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="77665-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="77665-109">4</span><span class="sxs-lookup"><span data-stu-id="77665-109">4</span></span></p></td>
<td><p><span data-ttu-id="77665-110">Отмена запросов на операцию, которая вызвала событие.</span><span class="sxs-lookup"><span data-stu-id="77665-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77665-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="77665-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="77665-112">3</span><span class="sxs-lookup"><span data-stu-id="77665-112">3</span></span></p></td>
<td><p><span data-ttu-id="77665-113">Указывает, что операция не могут запрашивать отмену ожидающие операции.</span><span class="sxs-lookup"><span data-stu-id="77665-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77665-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="77665-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="77665-115">2</span><span class="sxs-lookup"><span data-stu-id="77665-115">2</span></span></p></td>
<td><p><span data-ttu-id="77665-116">Указывает, что операция, которая вызвала событие сбой из-за ошибки или ошибки.</span><span class="sxs-lookup"><span data-stu-id="77665-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77665-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="77665-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="77665-118">1</span><span class="sxs-lookup"><span data-stu-id="77665-118">1</span></span></p></td>
<td><p><span data-ttu-id="77665-119">Указывает, что операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="77665-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77665-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="77665-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="77665-121">5</span><span class="sxs-lookup"><span data-stu-id="77665-121">5</span></span></p></td>
<td><p><span data-ttu-id="77665-122">До завершения выполнения метода события не позволяет последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="77665-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77665-123">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="77665-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="77665-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="77665-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77665-125">Constant</span><span class="sxs-lookup"><span data-stu-id="77665-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77665-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="77665-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77665-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="77665-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77665-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="77665-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77665-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="77665-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77665-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="77665-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

