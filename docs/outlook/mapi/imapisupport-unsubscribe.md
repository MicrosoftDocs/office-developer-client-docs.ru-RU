---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421216"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отменяет ответственность за отправку уведомлений, которые ранее были установлены с помощью вызова метода [IMAPISupport::Subscribe.](imapisupport-subscribe.md) 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Номер подключения без номеров, который представляет регистрацию уведомлений, ранее установленную с помощью **IMAPISupport::Subscribe.**
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений была отменена.
    
MAPI_E_NOT_FOUND 
  
> Номер подключения, переданный в  _параметре ulConnection,_ не существует. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::Unsubscribe** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг **звонят отменить** подписку, чтобы отменить регистрацию уведомлений, ранее настроенную **подпиской.** **Отмена подписки** отменяет регистрацию, освобождая указатель на оглавение, переданный в **вызове Subscribe.** 
  
Как правило, метод **IUnknown::Release** приемника рекомендации вызываем во время вызова **"Отписаться".** Однако если другой поток вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемника рекомендации, вызов **release** откладывается до тех пор, пока не будет возвращен метод **OnNotify.** 
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

