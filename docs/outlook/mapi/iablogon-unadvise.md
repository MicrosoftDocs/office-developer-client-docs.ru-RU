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
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запрос уведомления, которые ранее были настроены с помощью вызова метода [IABLogon::Advise](iablogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Номер подключения, связанный с регистрацию active уведомлений. Предыдущий вызов **уведомлений** необходимо возвращается значение _ulConnection_.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений успешно отменена.
    
## <a name="remarks"></a>Замечания

MAPI вызывает метод **Unadvise** для отмены регистрации уведомлений для контейнера, системы обмена сообщениями пользователя или объект списка рассылки. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Реализация **Unadvise** будут зависеть от ли поддерживать уведомлений с помощью интерфейса MAPI или вручную. Если поддерживает MAPI, вызовите метод [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) для отмены регистрации. Если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник уведомлений, его можно отложить до вернул **OnNotify** . 
  
Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md). Для получения сведений об использовании [IMAPISupport: IUnknown](imapisupportiunknown.md) методы для поддержки уведомлений, видеть [Поддержка уведомления о событии](supporting-event-notification.md).
  
## <a name="see-also"></a>См. также



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

