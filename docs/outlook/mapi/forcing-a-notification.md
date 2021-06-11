---
title: Принуждение к уведомлению
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
# <a name="forcing-a-notification"></a>Принуждение к уведомлению

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Когда поставщики услуг используют методы [IMAPISupport : IUnknown](imapisupportiunknown.md) для уведомления, MAPI доставляет уведомления с помощью скрытого окна и соответствующей процедуры окна. Для каждого процесса получения уведомления MAPI публикует специальное сообщение в скрытое окно. Это сообщение называется с постоянной **szMAPINotificationMsg,** которая определяется в MAPIDEFS.H. 
  
Вы получаете эти уведомления, когда процедура окна скрытого окна обрабатывает **сообщение szMAPINotificationMsg.** Чтобы гарантировать доставку уведомлений, необходимо дождаться и отправить это **сообщение szMAPINotificationMsg.** Реализация логики для этого может быть выполнена довольно просто, но MAPI предоставляет точку входа в DLL MAPI под названием [HrDispatchNotifications,](hrdispatchnotifications.md) чтобы сделать обработку еще проще. Позвоните **в HrDispatchNotifications** следующим образом, чтобы получать уведомления в клиенте: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


