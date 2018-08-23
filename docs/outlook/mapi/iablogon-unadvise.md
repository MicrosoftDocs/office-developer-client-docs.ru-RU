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
ms.openlocfilehash: 3fbf8b423cfd4206a0143b5639c85dbcacce2fae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570984"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="9757b-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="9757b-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="9757b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9757b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9757b-105">Запрос уведомления, которые ранее были настроены с помощью вызова метода [IABLogon::Advise](iablogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="9757b-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="9757b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9757b-106">Parameters</span></span>

 <span data-ttu-id="9757b-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="9757b-107">_ulConnection_</span></span>
  
> <span data-ttu-id="9757b-108">[in] Номер подключения, связанный с регистрацию active уведомлений.</span><span class="sxs-lookup"><span data-stu-id="9757b-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="9757b-109">Предыдущий вызов **уведомлений** необходимо возвращается значение _ulConnection_.</span><span class="sxs-lookup"><span data-stu-id="9757b-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9757b-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9757b-110">Return value</span></span>

<span data-ttu-id="9757b-111">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="9757b-111">S_OK</span></span> 
  
> <span data-ttu-id="9757b-112">Регистрация уведомлений успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="9757b-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9757b-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="9757b-113">Remarks</span></span>

<span data-ttu-id="9757b-114">MAPI вызывает метод **Unadvise** для отмены регистрации уведомлений для контейнера, системы обмена сообщениями пользователя или объект списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="9757b-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9757b-115">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="9757b-115">Notes to implementers</span></span>

<span data-ttu-id="9757b-116">Реализация **Unadvise** будут зависеть от ли поддерживать уведомлений с помощью интерфейса MAPI или вручную.</span><span class="sxs-lookup"><span data-stu-id="9757b-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="9757b-117">Если поддерживает MAPI, вызовите метод [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="9757b-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="9757b-118">Если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник уведомлений, его можно отложить до вернул **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="9757b-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="9757b-119">Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="9757b-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="9757b-120">Для получения сведений об использовании [IMAPISupport: IUnknown](imapisupportiunknown.md) методы для поддержки уведомлений, видеть [Поддержка уведомления о событии](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="9757b-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9757b-121">См. также</span><span class="sxs-lookup"><span data-stu-id="9757b-121">See also</span></span>



[<span data-ttu-id="9757b-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="9757b-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="9757b-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="9757b-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="9757b-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9757b-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

