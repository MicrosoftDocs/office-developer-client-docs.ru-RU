---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 01ea05eb864c78f3ded39ca3ebc62578076b9d37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584662"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="4d0c2-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="4d0c2-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="4d0c2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d0c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d0c2-105">Отменяет ответственность за отправки уведомлений, которое ранее было установлено с помощью вызова метода [IMAPISupport::Subscribe](imapisupport-subscribe.md) .</span><span class="sxs-lookup"><span data-stu-id="4d0c2-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4d0c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d0c2-106">Parameters</span></span>

 <span data-ttu-id="4d0c2-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="4d0c2-107">_ulConnection_</span></span>
  
> <span data-ttu-id="4d0c2-108">[in] Подключение ненулевое число, представляющее регистрации уведомлений, установленное ранее при помощи **IMAPISupport::Subscribe**.</span><span class="sxs-lookup"><span data-stu-id="4d0c2-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4d0c2-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4d0c2-109">Return value</span></span>

<span data-ttu-id="4d0c2-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4d0c2-110">S_OK</span></span> 
  
> <span data-ttu-id="4d0c2-111">Регистрация уведомлений отменена.</span><span class="sxs-lookup"><span data-stu-id="4d0c2-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="4d0c2-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4d0c2-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4d0c2-113">Номер соединения, переданной в параметре _ulConnection_ не существует.</span><span class="sxs-lookup"><span data-stu-id="4d0c2-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4d0c2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d0c2-114">Remarks</span></span>

<span data-ttu-id="4d0c2-115">Метод **IMAPISupport::Unsubscribe** применяется для всех объектов поддержки поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="4d0c2-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="4d0c2-116">Поставщики услуг вызов **отказа от подписки** для отмены регистрации уведомлений, ранее настроить по **подписке на**.</span><span class="sxs-lookup"><span data-stu-id="4d0c2-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="4d0c2-117">**Отказа от подписки** отменяет регистрацию освободить указатель приемник уведомлений, переданный **подписки на** звонок.</span><span class="sxs-lookup"><span data-stu-id="4d0c2-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="4d0c2-118">Как правило, вызывается метод **функции IUnknown::Release** приемник уведомлений во время вызова **отказа от подписки** .</span><span class="sxs-lookup"><span data-stu-id="4d0c2-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="4d0c2-119">Тем не менее если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемник уведомлений, вызов **выпуске** откладывается до возвращения методом **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="4d0c2-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d0c2-120">См. также</span><span class="sxs-lookup"><span data-stu-id="4d0c2-120">See also</span></span>



[<span data-ttu-id="4d0c2-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="4d0c2-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="4d0c2-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="4d0c2-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="4d0c2-123">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d0c2-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

