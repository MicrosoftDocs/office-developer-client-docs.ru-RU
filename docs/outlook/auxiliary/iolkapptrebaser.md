---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Поддерживает повторного размещения en встреч в папке календаря.
ms.openlocfilehash: 57ca59121f74c7b64a84282c7493e4aed3179f7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807869"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="d0fa5-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="d0fa5-103">IOlkApptRebaser</span></span>

<span data-ttu-id="d0fa5-104">Поддерживает повторного размещения en встреч в папке календаря.</span><span class="sxs-lookup"><span data-stu-id="d0fa5-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d0fa5-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d0fa5-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0fa5-106">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="d0fa5-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="d0fa5-107">**Интерфейс IUnknown**</span><span class="sxs-lookup"><span data-stu-id="d0fa5-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="d0fa5-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d0fa5-108">Header file:</span></span>  <br/> |<span data-ttu-id="d0fa5-109">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="d0fa5-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="d0fa5-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="d0fa5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="d0fa5-111">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="d0fa5-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="d0fa5-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="d0fa5-112">Called by:</span></span>  <br/> |<span data-ttu-id="d0fa5-113">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="d0fa5-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="d0fa5-114">Предоставляется для:</span><span class="sxs-lookup"><span data-stu-id="d0fa5-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="d0fa5-115">Объект сдвига Outlook</span><span class="sxs-lookup"><span data-stu-id="d0fa5-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d0fa5-116">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="d0fa5-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0fa5-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="d0fa5-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="d0fa5-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span><span class="sxs-lookup"><span data-stu-id="d0fa5-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="d0fa5-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="d0fa5-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="d0fa5-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span><span class="sxs-lookup"><span data-stu-id="d0fa5-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="d0fa5-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="d0fa5-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="d0fa5-122">Начинается задач для повторного размещения встречи en список встреч, обычно получили от **EndEnumerateAppointments**.</span><span class="sxs-lookup"><span data-stu-id="d0fa5-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="d0fa5-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="d0fa5-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="d0fa5-124">Waits for appointment rebasing to complete and retrieves the results.</span><span class="sxs-lookup"><span data-stu-id="d0fa5-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0fa5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d0fa5-125">See also</span></span>

- [<span data-ttu-id="d0fa5-126">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="d0fa5-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

