---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435938"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Область применения**: Outlook 2013 | Outlook 2016 
  
Отправляет уведомление о указанном событии источнику консультаций, который первоначально зарегистрировался для уведомления с помощью [метода IMAPISupport::Subscribe.](imapisupport-subscribe.md) 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

_lpKey_
  
> [in] Указатель на ключ уведомления для объекта-источника консультации. Параметр  _lpKey не_ может быть NULL. 
    
_cNotification_
  
> [in] Количество структур уведомлений, на которые указывает параметр _lpNotifications._ 
    
_lpNotifications_
  
> [in] Указатель на массив структур [УВЕДОМЛЕНий,](notification.md) описывающих ожидающих уведомлений. 
    
_lpulFlags_
  
> [in, out] Битмашка флагов, которые контролируют процесс уведомления. На входе можно установить следующий флаг:
    
  - MAPI_UNICODE 
    
    > Строки в структурах уведомлений, на которые указывают  _lpNotifications,_ находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 

    На выходе MAPI может установить следующий флаг:
        
  - NOTIFY_CANCELED 
    
    > Функция вызова отменяет синхронное уведомление.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомления были успешно сгенерированы.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::Notify** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг  вызывают Уведомление о том, что MAPI создает уведомление для приемника консультаций, который ранее зарегистрировался для уведомления с помощью **метода IMAPISupport::Subscribe.** 
  
**Уведомите** копии структур, на которые указывает параметр _lpNotifications,_ в память и вызывает соответствующий метод [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md) Когда **OnNotify** завершается с уведомлением, он освобождает участвуют памяти. Вызываемой не требуется выделять память; MAPI выполняет все необходимые выделения памяти. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Ключ уведомления, переданный в _параметре lpKey,_ должен быть идентичен клавише, переданной _в lpKey_ методу **IMAPISupport::Subscribe.** Многие поставщики используют идентификатор входа источника консультаций в качестве ключа, но другие данные, например путь к файлу, можно использовать. MAPI использует этот ключ, чтобы найти все регистрации для уведомлений в выявленных источниках консультаций. 
  
Убедитесь, что участник **lpEntryID** в структуре уведомлений был настроен на долгосрочный идентификатор записи. 
  
Если вы установите флаг NOTIFY_SYNC в вызове **Подписка** для любого из ожидающих уведомлений,  перед возвращением уведомите об этом функции обратного вызова метода **IMAPIAdviseSink::OnNotify.** Раковина рекомендации может быть создана вручную или по вызову [HrAllocAdviseSink](hrallocadvisesink.md). Функция **HrAllocAdviseSink** позволяет вызываемой функции указать функцию вызова, уведомляемую о вызовах в рамках уведомления.  Функция вызова соответствует прототипу [NOTIFCALLBACK.](notifcallback.md) Функции обратного вызова, реализованные клиентами, всегда возвращаются S_OK; Функции обратного вызова, реализованные поставщиками услуг, могут CALLBACK_DISCONTINUE. 
  
Если функция обратного вызова возвращается CALLBACK_DISCONTINUE, MAPI прекращает отправку уведомлений и возвращает NOTIFY_CANCELED в _параметре lpulFlags_ метода **Notify.** Можно предположить, что процесс неактивный, и прекратить создание уведомлений для этого процесса. Если **Уведомление** возвращает 0 в  _lpulFlags,_ процесс по-прежнему активен, и вы должны продолжать отправлять уведомления, как это необходимо.
  
При использовании синхронных уведомлений будьте осторожны, чтобы избежать ситуаций с затором.
  
Дополнительные сведения о процессе уведомления см. в сообщении [события в MAPI.](event-notification-in-mapi.md) 
  
## <a name="see-also"></a>См. также

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [�����������](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Каноническое свойство PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

