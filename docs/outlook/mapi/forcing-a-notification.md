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
# <a name="forcing-a-notification"></a>Принудительная отправка уведомления

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Когда поставщики услуг используют [IMAPISupport: IUnknown](imapisupportiunknown.md) методы для уведомления, MAPI доставляет уведомления с помощью скрытое окно и соответствующие процедуры окна. Для каждого процесса получать уведомления о MAPI публикует сообщение специальные скрытое окно. С постоянным **szMAPINotificationMsg** , которое определяется в MAPIDEFS именем этого сообщения. З. 
  
Вы получаете такие уведомления, когда скрытое окно window процедура обрабатывает сообщение **szMAPINotificationMsg** . Чтобы гарантировать доставку уведомлений, необходимые для ожидания и отправки этого сообщения **szMAPINotificationMsg** . Реализация логики для этого можно выполнить довольно просто, но MAPI предоставляет точки входа в MAPI DLL называется [HrDispatchNotifications](hrdispatchnotifications.md) , чтобы сделать обработки еще проще. Вызов **HrDispatchNotifications** следующим образом, чтобы получать уведомления в клиенте: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


