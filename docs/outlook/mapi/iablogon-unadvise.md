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
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424079"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отменяет уведомления, которые ранее были настроены с помощью вызова метода [IABLogon::Advise.](iablogon-advise.md) 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in] Номер подключения, связанный с активной регистрацией уведомлений. Предыдущий вызов **в "Совет"** должен был вернуть значение _ulConnection._
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений была успешно отменена.
    
## <a name="remarks"></a>Примечания

MAPI вызывает **метод Unadvise** для отмены регистрации уведомлений для объекта контейнера, пользователя обмена сообщениями или списка рассылки. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация **Unadvise будет** зависеть от того, поддерживаете ли вы уведомление с помощью MAPI или вручную. Если MAPI предоставляет вашу поддержку, позвоните по [методу IMAPISupport::Unsubscribe,](imapisupport-unsubscribe.md) чтобы отменить регистрацию. Если другой поток вызывает метод [IMAPIAdviseSink::OnNotify,](imapiadvisesink-onnotify.md) его можно отложить до тех пор, пока **OnNotify** не вернется. 
  
Дополнительные сведения о процессе уведомления см. в сообщении [события в MAPI.](event-notification-in-mapi.md) Сведения о том, как использовать [методы IMAPISupport: IUnknown](imapisupportiunknown.md) для поддержки уведомления, см. в [рубрике Уведомление о событиях поддержки.](supporting-event-notification.md)
  
## <a name="see-also"></a>См. также



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

