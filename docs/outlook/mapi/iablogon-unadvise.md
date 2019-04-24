---
title: Иаблогонунадвисе
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348883"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="20229-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="20229-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="20229-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20229-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20229-105">ОтМеняет уведомления, которые ранее были настроены с помощью вызова метода [иаблогон:: Advise](iablogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="20229-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="20229-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20229-106">Parameters</span></span>

 <span data-ttu-id="20229-107">_Улконнектион_</span><span class="sxs-lookup"><span data-stu-id="20229-107">_ulConnection_</span></span>
  
> <span data-ttu-id="20229-108">возврата Номер подключения, связанный с активной регистрацией уведомлений.</span><span class="sxs-lookup"><span data-stu-id="20229-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="20229-109">Предыдущим вызовом метода **advise** должно быть возвращено значение _улконнектион_.</span><span class="sxs-lookup"><span data-stu-id="20229-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20229-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20229-110">Return value</span></span>

<span data-ttu-id="20229-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="20229-111">S_OK</span></span> 
  
> <span data-ttu-id="20229-112">Регистрация уведомления успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="20229-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20229-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="20229-113">Remarks</span></span>

<span data-ttu-id="20229-114">MAPI вызывает метод **unadvise** для отмены регистрации уведомления для контейнера, пользователя обмена сообщениями или объекта списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="20229-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="20229-115">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="20229-115">Notes to implementers</span></span>

<span data-ttu-id="20229-116">Ваша реализация метода **unadvise** будет зависеть от того, поддерживает ли вы уведомление с помощью MAPI или вручную.</span><span class="sxs-lookup"><span data-stu-id="20229-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="20229-117">Если поддержка MAPI обеспечивает поддержку, вызовите метод [имаписуппорт:: unsubscribe](imapisupport-unsubscribe.md) для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="20229-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="20229-118">Если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) приемника уведомлений, его можно задержать, пока не будет \*\*\*\* возвращено значение OnNotify.</span><span class="sxs-lookup"><span data-stu-id="20229-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="20229-119">Дополнительные сведения о процессе уведомления можно найти в статье [уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="20229-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="20229-120">Сведения об использовании методов [имаписуппорт: IUnknown](imapisupportiunknown.md) для поддержки уведомлений см. [](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="20229-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20229-121">См. также</span><span class="sxs-lookup"><span data-stu-id="20229-121">See also</span></span>



[<span data-ttu-id="20229-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="20229-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="20229-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="20229-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="20229-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20229-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

