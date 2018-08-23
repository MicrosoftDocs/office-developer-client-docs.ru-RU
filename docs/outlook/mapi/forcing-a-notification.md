---
title: Принудительная отправка уведомления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5affce8ab7a8b08019816ad9485641c401dd80c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578775"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="e41e9-103">Принудительная отправка уведомления</span><span class="sxs-lookup"><span data-stu-id="e41e9-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="e41e9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e41e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e41e9-105">Когда поставщики услуг используют [IMAPISupport: IUnknown](imapisupportiunknown.md) методы для уведомления, MAPI доставляет уведомления с помощью скрытое окно и соответствующие процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="e41e9-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="e41e9-106">Для каждого процесса получать уведомления о MAPI публикует сообщение специальные скрытое окно.</span><span class="sxs-lookup"><span data-stu-id="e41e9-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="e41e9-107">С постоянным **szMAPINotificationMsg** , которое определяется в MAPIDEFS именем этого сообщения. З.</span><span class="sxs-lookup"><span data-stu-id="e41e9-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="e41e9-108">Вы получаете такие уведомления, когда скрытое окно window процедура обрабатывает сообщение **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="e41e9-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="e41e9-109">Чтобы гарантировать доставку уведомлений, необходимые для ожидания и отправки этого сообщения **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="e41e9-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="e41e9-110">Реализация логики для этого можно выполнить довольно просто, но MAPI предоставляет точки входа в MAPI DLL называется [HrDispatchNotifications](hrdispatchnotifications.md) , чтобы сделать обработки еще проще.</span><span class="sxs-lookup"><span data-stu-id="e41e9-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="e41e9-111">Вызов **HrDispatchNotifications** следующим образом, чтобы получать уведомления в клиенте:</span><span class="sxs-lookup"><span data-stu-id="e41e9-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


