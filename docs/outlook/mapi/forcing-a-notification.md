---
title: Принудительное уведомление
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 40fc763071f7113e222c6987dfd70fb7d89bab4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808468"
---
# <a name="forcing-a-notification"></a>Принудительное уведомление

  
  
**Применимо к**: Outlook 
  
Когда поставщики услуг используют [IMAPISupport: IUnknown](imapisupportiunknown.md) методы для уведомления, MAPI доставляет уведомления с помощью скрытое окно и соответствующие процедуры окна. Для каждого процесса получать уведомления о MAPI публикует сообщение специальные скрытое окно. С постоянным **szMAPINotificationMsg** , которое определяется в MAPIDEFS именем этого сообщения. З. 
  
Вы получаете такие уведомления, когда скрытое окно window процедура обрабатывает сообщение **szMAPINotificationMsg** . Чтобы гарантировать доставку уведомлений, необходимые для ожидания и отправки этого сообщения **szMAPINotificationMsg** . Реализация логики для этого можно выполнить довольно просто, но MAPI предоставляет точки входа в MAPI DLL называется [HrDispatchNotifications](hrdispatchnotifications.md) , чтобы сделать обработки еще проще. Вызов **HrDispatchNotifications** следующим образом, чтобы получать уведомления в клиенте: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


