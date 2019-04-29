---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Поддерживает переиндексацию встреч в папке "Календарь".
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410072"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="47c51-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="47c51-103">IOlkApptRebaser</span></span>

<span data-ttu-id="47c51-104">Поддерживает переиндексацию встреч в папке "Календарь".</span><span class="sxs-lookup"><span data-stu-id="47c51-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="47c51-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="47c51-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47c51-106">Наследование от:</span><span class="sxs-lookup"><span data-stu-id="47c51-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="47c51-107">**Интерфейс**</span><span class="sxs-lookup"><span data-stu-id="47c51-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="47c51-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="47c51-108">Header file:</span></span>  <br/> |<span data-ttu-id="47c51-109">тзмовелиб. h</span><span class="sxs-lookup"><span data-stu-id="47c51-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="47c51-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="47c51-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="47c51-111">тзмовелиб. dll</span><span class="sxs-lookup"><span data-stu-id="47c51-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="47c51-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="47c51-112">Called by:</span></span>  <br/> |<span data-ttu-id="47c51-113">Клиентские приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="47c51-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="47c51-114">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="47c51-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="47c51-115">Объект перебазового объекта Outlook</span><span class="sxs-lookup"><span data-stu-id="47c51-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="47c51-116">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="47c51-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47c51-117">**[Бегиненумератеаппоинтментс](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="47c51-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="47c51-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span><span class="sxs-lookup"><span data-stu-id="47c51-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="47c51-119">**[Енденумератеаппоинтментс](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="47c51-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="47c51-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span><span class="sxs-lookup"><span data-stu-id="47c51-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="47c51-121">**[Бегинребасеаппоинтментс](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="47c51-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="47c51-122">Начинает задачу, которая передается из списка встреч, обычно получаемых из **енденумератеаппоинтментс**.</span><span class="sxs-lookup"><span data-stu-id="47c51-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="47c51-123">**[Ендребасеаппоинтментс](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="47c51-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="47c51-124">Waits for appointment rebasing to complete and retrieves the results.</span><span class="sxs-lookup"><span data-stu-id="47c51-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47c51-125">См. также</span><span class="sxs-lookup"><span data-stu-id="47c51-125">See also</span></span>

- [<span data-ttu-id="47c51-126">About rebasing calendars programmatically for Daylight Saving Time</span><span class="sxs-lookup"><span data-stu-id="47c51-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

