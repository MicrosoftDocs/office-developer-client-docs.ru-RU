---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Поддерживает переостережку встреч в папке календаря.
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410072"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="cfc6b-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="cfc6b-103">IOlkApptRebaser</span></span>

<span data-ttu-id="cfc6b-104">Поддерживает переостережку встреч в папке календаря.</span><span class="sxs-lookup"><span data-stu-id="cfc6b-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cfc6b-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="cfc6b-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cfc6b-106">Наследуется от:</span><span class="sxs-lookup"><span data-stu-id="cfc6b-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="cfc6b-107">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="cfc6b-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="cfc6b-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cfc6b-108">Header file:</span></span>  <br/> |<span data-ttu-id="cfc6b-109">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="cfc6b-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="cfc6b-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="cfc6b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="cfc6b-111">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="cfc6b-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="cfc6b-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="cfc6b-112">Called by:</span></span>  <br/> |<span data-ttu-id="cfc6b-113">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="cfc6b-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="cfc6b-114">В:</span><span class="sxs-lookup"><span data-stu-id="cfc6b-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="cfc6b-115">Объект outlook rebasing</span><span class="sxs-lookup"><span data-stu-id="cfc6b-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cfc6b-116">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="cfc6b-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cfc6b-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="cfc6b-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="cfc6b-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span><span class="sxs-lookup"><span data-stu-id="cfc6b-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="cfc6b-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="cfc6b-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="cfc6b-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span><span class="sxs-lookup"><span data-stu-id="cfc6b-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="cfc6b-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="cfc6b-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="cfc6b-122">Начинает задачу по переоплате встреч с учетом списка встреч, обычно полученных из **EndEnumerateAppointments.**</span><span class="sxs-lookup"><span data-stu-id="cfc6b-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="cfc6b-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="cfc6b-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="cfc6b-124">Waits for appointment rebasing to complete and retrieves the results.</span><span class="sxs-lookup"><span data-stu-id="cfc6b-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cfc6b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="cfc6b-125">See also</span></span>

- [<span data-ttu-id="cfc6b-126">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="cfc6b-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

