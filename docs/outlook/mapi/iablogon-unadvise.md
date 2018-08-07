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
ms.openlocfilehash: d9f69098f9c53e75dea6f485248d61d277e181c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808733"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Относится к**: Outlook 
  
Запрос уведомления, которые ранее были настроены с помощью вызова метода [IABLogon::Advise](iablogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Номер подключения, связанный с регистрацию active уведомлений. Предыдущий вызов **уведомлений** необходимо возвращается значение _ulConnection_.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Регистрация уведомлений успешно отменена.
    
## <a name="remarks"></a>Замечания

MAPI вызывает метод **Unadvise** для отмены регистрации уведомлений для контейнера, системы обмена сообщениями пользователя или объект списка рассылки. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация **Unadvise** будут зависеть от ли поддерживать уведомлений с помощью интерфейса MAPI или вручную. Если поддерживает MAPI, вызовите метод [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) для отмены регистрации. Если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник уведомлений, его можно отложить до вернул **OnNotify** . 
  
Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md). Для получения сведений об использовании [IMAPISupport: IUnknown](imapisupportiunknown.md) методы для поддержки уведомлений, видеть [Поддержка уведомления о событии](supporting-event-notification.md).
  
## <a name="see-also"></a>См. также



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

