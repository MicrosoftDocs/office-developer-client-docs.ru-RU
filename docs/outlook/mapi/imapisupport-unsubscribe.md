---
title: Имаписуппортунсубскрибе
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341267"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
ОтМеняет ответственность за отправку уведомлений, которые были установлены ранее при вызове метода [имаписуппорт:: Subscribe](imapisupport-subscribe.md) . 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Параметры

 _Улконнектион_
  
> возврата Ненулевой номер подключения, представляющий регистрацию уведомления, предварительно установленную через **имаписуппорт:: Subscribe**.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомления отменена.
    
МАПИ_Е_НОТ_ФАУНД 
  
> Номер подключения, переданный в параметре _улконнектион_ , не существует. 
    
## <a name="remarks"></a>Комментарии

Метод **имаписуппорт:: unsubscribe** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг отменяют подписываться на отмену регистрации уведомлений, предварительно настроенных подПискум. **** **** **Unsubscribe** отменяет регистрацию, освобождая указатель приемника уведомлений, переданный в вызове **Subscribe** . 
  
Как правило, метод **IUnknown:: Release** приемника уведомлений вызывается во время **** вызова unsubscribe. Тем не менее, если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) для объекта приемника уведомлений, вызов **освобождения** задерживается до возвращения метода **OnNotify** . 
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

