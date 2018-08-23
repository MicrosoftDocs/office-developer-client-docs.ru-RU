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
ms.openlocfilehash: 60c5d7e980d1dc4d4263a2be2267008dbee1fd4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594700"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="ee197-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="ee197-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="ee197-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee197-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee197-105">Принудительное диспетчеризации всех уведомлений, помещенных в очередь.</span><span class="sxs-lookup"><span data-stu-id="ee197-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee197-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ee197-106">Header file:</span></span>  <br/> |<span data-ttu-id="ee197-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ee197-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ee197-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="ee197-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ee197-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ee197-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ee197-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="ee197-110">Called by:</span></span>  <br/> |<span data-ttu-id="ee197-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="ee197-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ee197-112">���������</span><span class="sxs-lookup"><span data-stu-id="ee197-112">Parameters</span></span>

 <span data-ttu-id="ee197-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee197-113">_ulFlags_</span></span>
  
> <span data-ttu-id="ee197-114">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="ee197-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ee197-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="ee197-115">Return value</span></span>

<span data-ttu-id="ee197-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="ee197-116">S_OK</span></span>
  
> <span data-ttu-id="ee197-117">Все уведомления о помещенных в очередь отправки.</span><span class="sxs-lookup"><span data-stu-id="ee197-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="ee197-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="ee197-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="ee197-119">WM_QUIT, WM_QUERYENDSESSION или WM_ENDSESSION был получен.</span><span class="sxs-lookup"><span data-stu-id="ee197-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="ee197-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ee197-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="ee197-121">Не удалось инициализировать MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee197-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee197-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="ee197-122">Remarks</span></span>

<span data-ttu-id="ee197-123">Функция **HrDispatchNotifications** вызывает MAPI для отправки всех уведомлений, которые в настоящее время в очереди в модуль уведомлений MAPI без ожидания отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="ee197-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="ee197-124">Это может иметь положительный эффект на использование памяти.</span><span class="sxs-lookup"><span data-stu-id="ee197-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="ee197-125">Для получения дополнительных сведений см [принудительным уведомление](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="ee197-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee197-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ee197-126">Notes to callers</span></span>

<span data-ttu-id="ee197-127">Некоторые приложения дождитесь сообщение уведомления в цикле времени ожидания, с помощью Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) и [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) функций.</span><span class="sxs-lookup"><span data-stu-id="ee197-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) and [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="ee197-128">На всех, кроме быстрым платформ такие приложения могут возникнуть низким быстродействием или даже блокировки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ee197-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="ee197-129">С помощью **HrDispatchNotifications** не только уменьшает кода, но повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="ee197-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

