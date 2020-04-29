---
title: Принудительное уведомление
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 54eaf9e67da1b520896122c937508a90700a0b84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433285"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="f3f4a-103">Принудительное уведомление</span><span class="sxs-lookup"><span data-stu-id="f3f4a-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="f3f4a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3f4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3f4a-105">Когда поставщики услуг используют методы [имаписуппорт: IUnknown](imapisupportiunknown.md) для уведомлений, MAPI доставляет уведомления с помощью скрытого окна и соответствующей процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="f3f4a-106">Для каждого процесса, который должен получать уведомление, MAPI отправляет специальное сообщение в скрытое окно.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="f3f4a-107">Этому сообщению присвоено значение константы **сзмапинотификатионмсг** , которое определено в MAPIDEFS. Высоты.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="f3f4a-108">Эти уведомления появляются, когда в окне скрытого окна обрабатывается сообщение **сзмапинотификатионмсг** .</span><span class="sxs-lookup"><span data-stu-id="f3f4a-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="f3f4a-109">Чтобы гарантировать доставку уведомлений, необходимо дождаться и отправить это сообщение **сзмапинотификатионмсг** .</span><span class="sxs-lookup"><span data-stu-id="f3f4a-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="f3f4a-110">Реализация логики для достижения этого можно выполнить довольно просто, но MAPI предоставляет точку входа в библиотеку DLL MAPI под названием [хрдиспатчнотификатионс](hrdispatchnotifications.md) , чтобы сделать обработку еще проще.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="f3f4a-111">Для получения уведомлений в клиенте вызовите **хрдиспатчнотификатионс** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f3f4a-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


