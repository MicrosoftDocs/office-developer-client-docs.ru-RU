---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424079"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="475ee-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="475ee-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="475ee-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="475ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="475ee-105">Отменяет уведомления, которые ранее были настроены с помощью вызова метода [IABLogon::Advise.](iablogon-advise.md)</span><span class="sxs-lookup"><span data-stu-id="475ee-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="475ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="475ee-106">Parameters</span></span>

 <span data-ttu-id="475ee-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="475ee-107">_ulConnection_</span></span>
  
> <span data-ttu-id="475ee-108">[in] Номер подключения, связанный с регистрацией активных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="475ee-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="475ee-109">Предыдущий вызов **"Сообщить"** должен возвращать значение _ulConnection._</span><span class="sxs-lookup"><span data-stu-id="475ee-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="475ee-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="475ee-110">Return value</span></span>

<span data-ttu-id="475ee-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="475ee-111">S_OK</span></span> 
  
> <span data-ttu-id="475ee-112">Регистрация уведомлений успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="475ee-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="475ee-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="475ee-113">Remarks</span></span>

<span data-ttu-id="475ee-114">MAPI вызывает метод **Unadvise** для отмены регистрации уведомлений для объекта контейнера, пользователя обмена сообщениями или списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="475ee-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="475ee-115">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="475ee-115">Notes to implementers</span></span>

<span data-ttu-id="475ee-116">Реализация **Unadvise** будет зависеть от того, поддерживаете ли вы уведомление с помощью справки MAPI или вручную.</span><span class="sxs-lookup"><span data-stu-id="475ee-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="475ee-117">Если mapI предоставляет поддержку, вызовите метод [IMAPISupport::Unsubscribe,](imapisupport-unsubscribe.md) чтобы отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="475ee-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="475ee-118">Если другой поток вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемника рекомендации, его можно отложить до тех пор, пока **OnNotify** не возвратит его.</span><span class="sxs-lookup"><span data-stu-id="475ee-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="475ee-119">Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="475ee-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="475ee-120">Сведения об использовании методов [IMAPISupport : IUnknown](imapisupportiunknown.md) для поддержки уведомлений см. в соответствующем [уведомлении.](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="475ee-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="475ee-121">См. также</span><span class="sxs-lookup"><span data-stu-id="475ee-121">See also</span></span>



[<span data-ttu-id="475ee-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="475ee-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="475ee-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="475ee-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="475ee-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="475ee-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

