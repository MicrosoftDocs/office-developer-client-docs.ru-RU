---
title: Евентстатусенум (Справочник по базам данных Access на компьютере)
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
# <a name="eventstatusenum"></a><span data-ttu-id="914e0-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="914e0-102">EventStatusEnum</span></span>

<span data-ttu-id="914e0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="914e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="914e0-104">Указывает текущее состояние выполнения события.</span><span class="sxs-lookup"><span data-stu-id="914e0-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="914e0-105">Константа</span><span class="sxs-lookup"><span data-stu-id="914e0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="914e0-106">Значение</span><span class="sxs-lookup"><span data-stu-id="914e0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="914e0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="914e0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="914e0-108"><strong>адстатусканцел</strong></span><span class="sxs-lookup"><span data-stu-id="914e0-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="914e0-109">4 </span><span class="sxs-lookup"><span data-stu-id="914e0-109">4</span></span></p></td>
<td><p><span data-ttu-id="914e0-110">Запрашивает отмену операции, которая привела к возникновению события.</span><span class="sxs-lookup"><span data-stu-id="914e0-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="914e0-111"><strong>адстатускантдени</strong></span><span class="sxs-lookup"><span data-stu-id="914e0-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="914e0-112">4</span><span class="sxs-lookup"><span data-stu-id="914e0-112">3</span></span></p></td>
<td><p><span data-ttu-id="914e0-113">Указывает, что операция не может запросить отмену ожидающей операции.</span><span class="sxs-lookup"><span data-stu-id="914e0-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="914e0-114"><strong>адстатусеррорсоккурред</strong></span><span class="sxs-lookup"><span data-stu-id="914e0-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="914e0-115">2</span><span class="sxs-lookup"><span data-stu-id="914e0-115">2</span></span></p></td>
<td><p><span data-ttu-id="914e0-116">Указывает, что операция, вызвавшая событие, не удалась из-за ошибки или ошибок.</span><span class="sxs-lookup"><span data-stu-id="914e0-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="914e0-117"><strong>адстатусок</strong></span><span class="sxs-lookup"><span data-stu-id="914e0-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="914e0-118">1,1</span><span class="sxs-lookup"><span data-stu-id="914e0-118">1</span></span></p></td>
<td><p><span data-ttu-id="914e0-119">Указывает, что операция, вызвавшая событие, выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="914e0-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="914e0-120"><strong>адстатусунвантедевент</strong></span><span class="sxs-lookup"><span data-stu-id="914e0-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="914e0-121">5 </span><span class="sxs-lookup"><span data-stu-id="914e0-121">5</span></span></p></td>
<td><p><span data-ttu-id="914e0-122">Предотвращает последующие уведомления до завершения выполнения метода события.</span><span class="sxs-lookup"><span data-stu-id="914e0-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="914e0-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="914e0-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="914e0-124">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="914e0-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="914e0-125">Константа</span><span class="sxs-lookup"><span data-stu-id="914e0-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="914e0-126">Адоенумс. Евентстатус. CANCEL</span><span class="sxs-lookup"><span data-stu-id="914e0-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="914e0-127">Адоенумс. Евентстатус. КАНТДЕНИ</span><span class="sxs-lookup"><span data-stu-id="914e0-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="914e0-128">Адоенумс. Евентстатус. ЕРРОРСОККУРРЕД</span><span class="sxs-lookup"><span data-stu-id="914e0-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="914e0-129">Адоенумс. Евентстатус. ОК</span><span class="sxs-lookup"><span data-stu-id="914e0-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="914e0-130">Адоенумс. Евентстатус. УНВАНТЕДЕВЕНТ</span><span class="sxs-lookup"><span data-stu-id="914e0-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

