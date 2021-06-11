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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отменяет ответственность за отправку уведомлений, ранее созданных с помощью вызова метода [IMAPISupport::Subscribe.](imapisupport-subscribe.md) 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in] Номер подключения nonzero, представляювший регистрацию уведомлений, ранее созданную через **IMAPISupport::Subscribe.**
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений была отменена.
    
MAPI_E_NOT_FOUND 
  
> Номер подключения, переданный в  _параметре ulConnection,_ не существует. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::Unsubscribe** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг призывают **отменить** регистрацию уведомлений, ранее созданную **подпиской.** **Отмена подписки** отменяет регистрацию, выпустив указатель на раковину рекомендации, переданный в **вызове Подписка.** 
  
Как правило, метод **IUnknown::Release** отозвать во время вызова **отписки.** Однако если другой поток находится в процессе вызова [метода IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для  объекта раковины рекомендации, вызов выпуска откладывается до тех пор, пока метод **OnNotify** не вернется. 
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

