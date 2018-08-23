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
ms.openlocfilehash: 01ea05eb864c78f3ded39ca3ebc62578076b9d37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584662"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Отменяет ответственность за отправки уведомлений, которое ранее было установлено с помощью вызова метода [IMAPISupport::Subscribe](imapisupport-subscribe.md) . 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Подключение ненулевое число, представляющее регистрации уведомлений, установленное ранее при помощи **IMAPISupport::Subscribe**.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Регистрация уведомлений отменена.
    
MAPI_E_NOT_FOUND 
  
> Номер соединения, переданной в параметре _ulConnection_ не существует. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::Unsubscribe** применяется для всех объектов поддержки поставщика службы. Поставщики услуг вызов **отказа от подписки** для отмены регистрации уведомлений, ранее настроить по **подписке на**. **Отказа от подписки** отменяет регистрацию освободить указатель приемник уведомлений, переданный **подписки на** звонок. 
  
Как правило, вызывается метод **функции IUnknown::Release** приемник уведомлений во время вызова **отказа от подписки** . Тем не менее если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемник уведомлений, вызов **выпуске** откладывается до возвращения методом **OnNotify** . 
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

