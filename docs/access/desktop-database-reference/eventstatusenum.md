---
title: EventStatusEnum (Справочник по для настольных баз данных Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 6e8408e2c73a60ae543bc9982de2f2547f54d1d2
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861535"
---
# <a name="eventstatusenum"></a><span data-ttu-id="82933-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="82933-102">EventStatusEnum</span></span>

<span data-ttu-id="82933-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="82933-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="82933-104">Указывает текущее состояние выполнения события.</span><span class="sxs-lookup"><span data-stu-id="82933-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82933-105">Константа</span><span class="sxs-lookup"><span data-stu-id="82933-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="82933-106">Значение</span><span class="sxs-lookup"><span data-stu-id="82933-106">Value</span></span></p></th>
<th><p><span data-ttu-id="82933-107">Описание</span><span class="sxs-lookup"><span data-stu-id="82933-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82933-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="82933-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="82933-109">4</span><span class="sxs-lookup"><span data-stu-id="82933-109">4</span></span></p></td>
<td><p><span data-ttu-id="82933-110">Отмена запросов на операцию, которая вызвала событие.</span><span class="sxs-lookup"><span data-stu-id="82933-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82933-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="82933-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="82933-112">3</span><span class="sxs-lookup"><span data-stu-id="82933-112">3</span></span></p></td>
<td><p><span data-ttu-id="82933-113">Указывает, что операция не могут запрашивать отмену ожидающие операции.</span><span class="sxs-lookup"><span data-stu-id="82933-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82933-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="82933-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="82933-115">2</span><span class="sxs-lookup"><span data-stu-id="82933-115">2</span></span></p></td>
<td><p><span data-ttu-id="82933-116">Указывает, что операция, которая вызвала событие сбой из-за ошибки или ошибки.</span><span class="sxs-lookup"><span data-stu-id="82933-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82933-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="82933-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="82933-118">1</span><span class="sxs-lookup"><span data-stu-id="82933-118">1</span></span></p></td>
<td><p><span data-ttu-id="82933-119">Указывает, что операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="82933-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82933-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="82933-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="82933-121">5</span><span class="sxs-lookup"><span data-stu-id="82933-121">5</span></span></p></td>
<td><p><span data-ttu-id="82933-122">До завершения выполнения метода события не позволяет последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="82933-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="82933-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="82933-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="82933-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="82933-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82933-125">Constant</span><span class="sxs-lookup"><span data-stu-id="82933-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82933-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="82933-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82933-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="82933-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82933-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="82933-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82933-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="82933-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82933-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="82933-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

