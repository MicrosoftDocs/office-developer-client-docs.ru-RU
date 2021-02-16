---
title: Принудительным уведомлением
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
# <a name="forcing-a-notification"></a>Принудительным уведомлением

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Когда поставщики услуг используют методы [IMAPISupport : IUnknown](imapisupportiunknown.md) для уведомлений, MAPI доставляет уведомления с помощью скрытого окна и соответствующей процедуры окна. Чтобы каждый процесс получил уведомление, MAPI публикует специальное сообщение в скрытом окне. Это сообщение называется константой **szMAPINotificationMsg,** определенной в MAPIDEFS.H. 
  
Вы получаете эти уведомления, когда процедура скрытого окна обрабатывает **сообщение szMAPINotificationMsg.** Чтобы гарантировать доставку уведомлений, необходимо дождаться и отправить это **сообщение szMAPINotificationMsg.** Реализовать логику для этого можно довольно просто, но MAPI предоставляет точку входа в DLL MAPI под названием [HrDispatchNotifications,](hrdispatchnotifications.md) чтобы упростить обработку. Вызовите **HrDispatchNotifications** следующим образом, чтобы получать уведомления в клиенте: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


