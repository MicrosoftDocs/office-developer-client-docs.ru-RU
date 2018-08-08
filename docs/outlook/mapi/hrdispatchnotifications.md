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
ms.openlocfilehash: 28afa338b37e747ed441a8767981b7e63808e741
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808672"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="d5f11-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="d5f11-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="d5f11-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5f11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5f11-105">Принудительное диспетчеризации всех уведомлений, помещенных в очередь.</span><span class="sxs-lookup"><span data-stu-id="d5f11-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5f11-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d5f11-106">Header file:</span></span>  <br/> |<span data-ttu-id="d5f11-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d5f11-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d5f11-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="d5f11-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d5f11-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d5f11-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d5f11-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="d5f11-110">Called by:</span></span>  <br/> |<span data-ttu-id="d5f11-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="d5f11-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d5f11-112">���������</span><span class="sxs-lookup"><span data-stu-id="d5f11-112">Parameters</span></span>

 <span data-ttu-id="d5f11-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5f11-113">_ulFlags_</span></span>
  
> <span data-ttu-id="d5f11-114">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d5f11-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d5f11-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d5f11-115">Return value</span></span>

<span data-ttu-id="d5f11-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d5f11-116">S_OK</span></span>
  
> <span data-ttu-id="d5f11-117">Все уведомления о помещенных в очередь отправки.</span><span class="sxs-lookup"><span data-stu-id="d5f11-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="d5f11-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d5f11-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="d5f11-119">WM_QUIT, WM_QUERYENDSESSION или WM_ENDSESSION был получен.</span><span class="sxs-lookup"><span data-stu-id="d5f11-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="d5f11-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="d5f11-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="d5f11-121">Не удалось инициализировать MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5f11-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5f11-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="d5f11-122">Remarks</span></span>

<span data-ttu-id="d5f11-123">Функция **HrDispatchNotifications** вызывает MAPI для отправки всех уведомлений, которые в настоящее время в очереди в модуль уведомлений MAPI без ожидания отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="d5f11-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="d5f11-124">Это может иметь положительный эффект на использование памяти.</span><span class="sxs-lookup"><span data-stu-id="d5f11-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="d5f11-125">Для получения дополнительных сведений см [принудительным уведомление](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="d5f11-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d5f11-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d5f11-126">Notes to callers</span></span>

<span data-ttu-id="d5f11-127">Некоторые приложения дождитесь сообщение уведомления в цикле времени ожидания, с помощью Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) и [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) функций.</span><span class="sxs-lookup"><span data-stu-id="d5f11-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) and [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="d5f11-128">На всех, кроме быстрым платформ такие приложения могут возникнуть низким быстродействием или даже блокировки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d5f11-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="d5f11-129">С помощью **HrDispatchNotifications** не только уменьшает кода, но повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="d5f11-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

