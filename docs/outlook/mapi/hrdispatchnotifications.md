---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348099"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="c71a1-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="c71a1-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="c71a1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c71a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c71a1-105">Принудительно отправляет уведомления из очереди.</span><span class="sxs-lookup"><span data-stu-id="c71a1-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c71a1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c71a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="c71a1-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="c71a1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c71a1-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c71a1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c71a1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c71a1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c71a1-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c71a1-110">Called by:</span></span>  <br/> |<span data-ttu-id="c71a1-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c71a1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c71a1-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c71a1-112">Parameters</span></span>

 <span data-ttu-id="c71a1-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c71a1-113">_ulFlags_</span></span>
  
> <span data-ttu-id="c71a1-114">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="c71a1-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c71a1-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c71a1-115">Return value</span></span>

<span data-ttu-id="c71a1-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c71a1-116">S_OK</span></span>
  
> <span data-ttu-id="c71a1-117">Все уведомления, помещенные в очередь, отправлены.</span><span class="sxs-lookup"><span data-stu-id="c71a1-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="c71a1-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="c71a1-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="c71a1-119">Получены WM_QUIT, WM_QUERYENDSESSION или WM_ENDSESSION.</span><span class="sxs-lookup"><span data-stu-id="c71a1-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="c71a1-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="c71a1-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="c71a1-121">MAPI не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="c71a1-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c71a1-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="c71a1-122">Remarks</span></span>

<span data-ttu-id="c71a1-123">Функция **хрдиспатчнотификатионс** заставляет MAPI отправлять все уведомления, находящиеся в очереди в обработчике уведомлений MAPI, без ожидания отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="c71a1-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="c71a1-124">Это может повлиять на использование памяти.</span><span class="sxs-lookup"><span data-stu-id="c71a1-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="c71a1-125">Для получения дополнительных сведений обратитесь к разделу " [принудительное уведомление](forcing-a-notification.md)".</span><span class="sxs-lookup"><span data-stu-id="c71a1-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c71a1-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c71a1-126">Notes to callers</span></span>

<span data-ttu-id="c71a1-127">Некоторые приложения ожидают сообщения с уведомлением в цикле ожидания с помощью функций Windows [пикмессаже](https://msdn.microsoft.com/library/ms644943.aspx) и [диспатчмессаже](https://msdn.microsoft.com/library/ms644934.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c71a1-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="c71a1-128">На всех платформах, кроме самых быстрых, такие приложения могут испытывать низкую производительность и даже заключать уведомления.</span><span class="sxs-lookup"><span data-stu-id="c71a1-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="c71a1-129">Использование **хрдиспатчнотификатионс** не только сокращает код, но повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="c71a1-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

