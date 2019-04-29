---
title: Иаблогонунадвисе
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
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424079"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
ОтМеняет уведомления, которые ранее были настроены с помощью вызова метода [иаблогон:: Advise](iablogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Параметры

 _Улконнектион_
  
> возврата Номер подключения, связанный с активной регистрацией уведомлений. Предыдущим вызовом метода **advise** должно быть возвращено значение _улконнектион_.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомления успешно отменена.
    
## <a name="remarks"></a>Примечания

MAPI вызывает метод **unadvise** для отмены регистрации уведомления для контейнера, пользователя обмена сообщениями или объекта списка рассылки. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Ваша реализация метода **unadvise** будет зависеть от того, поддерживает ли вы уведомление с помощью MAPI или вручную. Если поддержка MAPI обеспечивает поддержку, вызовите метод [имаписуппорт:: unsubscribe](imapisupport-unsubscribe.md) для отмены регистрации. Если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) приемника уведомлений, его можно задержать, пока не будет **** возвращено значение OnNotify. 
  
Дополнительные сведения о процессе уведомления можно найти в статье [уведомление о событии в MAPI](event-notification-in-mapi.md). Сведения об использовании методов [имаписуппорт: IUnknown](imapisupportiunknown.md) для поддержки уведомлений см. [](supporting-event-notification.md)
  
## <a name="see-also"></a>См. также



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

