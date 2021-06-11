---
title: 'IMAPIWaitResult : IUnknown'
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 26, 2021
ms.openlocfilehash: 67a0fffdd0ab6d4989c12568f4d89808ba5adc7a
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062041"
---
# <a name="imapiwaitresult--iunknown"></a><span data-ttu-id="82598-103">IMAPIWaitResult : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82598-103">IMAPIWaitResult : IUnknown</span></span>
  
<span data-ttu-id="82598-104">**Применяется к**: Outlook 2013 | Outlook 2016 | Outlook 2019 г.</span><span class="sxs-lookup"><span data-stu-id="82598-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="82598-105">Этот интерфейс используется пользователями IMAPIInitMonitor для управления, где происходит ожидание.</span><span class="sxs-lookup"><span data-stu-id="82598-105">This interface is used by consumers of IMAPIInitMonitor to control where the wait happens.</span></span> <span data-ttu-id="82598-106">Это позволяет им создавать объект на одном потоке и перемещать его другим потоком для выполнения фактического ожидания.</span><span class="sxs-lookup"><span data-stu-id="82598-106">It allows them create the object on one thread and move it another thread to perform the actual wait.</span></span>

## <a name="vtable-order"></a><span data-ttu-id="82598-107">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="82598-107">Vtable order</span></span>

| <span data-ttu-id="82598-108">функция</span><span class="sxs-lookup"><span data-stu-id="82598-108">function</span></span> | <span data-ttu-id="82598-109">description</span><span class="sxs-lookup"><span data-stu-id="82598-109">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="82598-110">HRESULT IMAPIWaitResult::End()</span><span class="sxs-lookup"><span data-stu-id="82598-110">HRESULT IMAPIWaitResult::End()</span></span>](imapiwaitresult-end.md)|<span data-ttu-id="82598-111">Вызвано, чтобы инициировать блокировку ожидания в потоке, где он называется, который не должен быть тем же потоком, который называется *IMAPIInitMonitor::BeginWait*.</span><span class="sxs-lookup"><span data-stu-id="82598-111">Called to initiate the blocking wait on the thread where it is called, which does not need to be the same thread that called *IMAPIInitMonitor::BeginWait*.</span></span>|

| <span data-ttu-id="82598-112">быстрая информация</span><span class="sxs-lookup"><span data-stu-id="82598-112">quick info</span></span> | <span data-ttu-id="82598-113">result</span><span class="sxs-lookup"><span data-stu-id="82598-113">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="82598-114">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="82598-114">Inherits from:</span></span>  <br/> |<span data-ttu-id="82598-115">IUnknown</span><span class="sxs-lookup"><span data-stu-id="82598-115">IUnknown</span></span>  <br/> |
|<span data-ttu-id="82598-116">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="82598-116">Implemented by:</span></span>  <br/> |  <span data-ttu-id="82598-117">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="82598-117">OLMAPI32.DLL</span></span><br/> |
|<span data-ttu-id="82598-118">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="82598-118">Called by:</span></span>  <br/> |<span data-ttu-id="82598-119">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="82598-119">Client applications</span></span>  <br/> |
|<span data-ttu-id="82598-120">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="82598-120">Interface identifier:</span></span>  <br/> |<span data-ttu-id="82598-121">IID_IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="82598-121">IID_IMAPIWaitResult</span></span>  <br/> |

## <a name="see-also"></a><span data-ttu-id="82598-122">См. также</span><span class="sxs-lookup"><span data-stu-id="82598-122">See also</span></span>

[<span data-ttu-id="82598-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="82598-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="82598-124">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="82598-124">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="82598-125">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82598-125">IMAPIInitMonitor : IUnknown</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="82598-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="82598-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
