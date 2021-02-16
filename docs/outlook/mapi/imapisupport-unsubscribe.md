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
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421216"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="f67a0-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="f67a0-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="f67a0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f67a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f67a0-105">Отменяет ответственность за отправку уведомлений, которые ранее были установлены с помощью вызова метода [IMAPISupport::Subscribe.](imapisupport-subscribe.md)</span><span class="sxs-lookup"><span data-stu-id="f67a0-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f67a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f67a0-106">Parameters</span></span>

 <span data-ttu-id="f67a0-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="f67a0-107">_ulConnection_</span></span>
  
> <span data-ttu-id="f67a0-108">[in] Номер подключения без номеров, который представляет регистрацию уведомлений, ранее установленную с помощью **IMAPISupport::Subscribe.**</span><span class="sxs-lookup"><span data-stu-id="f67a0-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f67a0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f67a0-109">Return value</span></span>

<span data-ttu-id="f67a0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f67a0-110">S_OK</span></span> 
  
> <span data-ttu-id="f67a0-111">Регистрация уведомлений была отменена.</span><span class="sxs-lookup"><span data-stu-id="f67a0-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="f67a0-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f67a0-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="f67a0-113">Номер подключения, переданный в  _параметре ulConnection,_ не существует.</span><span class="sxs-lookup"><span data-stu-id="f67a0-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f67a0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f67a0-114">Remarks</span></span>

<span data-ttu-id="f67a0-115">Метод **IMAPISupport::Unsubscribe** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="f67a0-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="f67a0-116">Поставщики услуг **звонят отменить** подписку, чтобы отменить регистрацию уведомлений, ранее настроенную **подпиской.**</span><span class="sxs-lookup"><span data-stu-id="f67a0-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="f67a0-117">**Отмена подписки** отменяет регистрацию, освобождая указатель на оглавение, переданный в **вызове Subscribe.**</span><span class="sxs-lookup"><span data-stu-id="f67a0-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="f67a0-118">Как правило, метод **IUnknown::Release** приемника рекомендации вызываем во время вызова **"Отписаться".**</span><span class="sxs-lookup"><span data-stu-id="f67a0-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="f67a0-119">Однако если другой поток вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемника рекомендации, вызов **release** откладывается до тех пор, пока не будет возвращен метод **OnNotify.**</span><span class="sxs-lookup"><span data-stu-id="f67a0-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f67a0-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f67a0-120">See also</span></span>



[<span data-ttu-id="f67a0-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f67a0-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f67a0-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="f67a0-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="f67a0-123">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f67a0-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

