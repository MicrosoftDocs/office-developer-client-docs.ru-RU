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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Отправляет уведомление об указанном событии источнику консультаций, который изначально зарегистрировался для уведомления с помощью метода [IMAPISupport::Subscribe.](imapisupport-subscribe.md) 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

_lpKey_
  
> [in] Указатель на ключ уведомления для объекта источника консультации. Параметр  _lpKey не может_ иметь NULL. 
    
_cNotification_
  
> [in] Количество структур уведомлений, на которые указывает параметр _lpNotifications._ 
    
_lpNotifications_
  
> [in] Указатель на массив структур [УВЕДОМЛЕНий,](notification.md) описывающих ожидающих уведомлений. 
    
_lpulFlags_
  
> [in, out] Битоваяmas флагов, которая управляет процессом уведомления. При вводе можно установить следующий флаг:
    
  - MAPI_UNICODE 
    
    > Строки в структурах уведомлений, на которые указывают  _lpNotifications,_ имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI. 

    В выходных данных MAPI может установить следующий флаг:
        
  - NOTIFY_CANCELED 
    
    > Функция callback отменила синхронное уведомление.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомления успешно созданы.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::Notify** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг вызывают **Notify,** чтобы попросить MAPI создать уведомление для приемника консультаций, который ранее зарегистрировался для уведомления с помощью метода **IMAPISupport::Subscribe.** 
  
**Уведомление** копирует структуры, на которые указывает параметр  _lpNotifications,_ в память и вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) соответствующего приемника рекомендации. Когда **onNotify** завершает работу с уведомлением, освобождается задействованная память. Вызываемой не нужно выделять память; MAPI выполняет все необходимые выделения памяти. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Ключ уведомления, переданный в _параметре lpKey,_ должен совпадать с ключом, переданным _в lpKey_ методу **IMAPISupport::Subscribe.** Многие поставщики используют идентификатор записи источника консультации в качестве ключа, но можно использовать другие данные, например путь к файлу. MAPI использует этот ключ для поиска всех регистраций для уведомлений в заданной источнике консультаций. 
  
Убедитесь, что для члена **lpEntryID** структуры уведомлений задан долгосрочный идентификатор записи. 
  
Если вы установите флаг NOTIFY_SYNC при вызове **Subscribe** для любого из ожидающих уведомлений,  уведомите перед возвратом вызов функции обратного вызова метода **IMAPIAdviseSink::OnNotify.** Вы можете создать тактовую ведомость вручную или с помощью вызова [HrAllocAdviseSink.](hrallocadvisesink.md) Функция **HrAllocAdviseSink** позволяет вызываемой функции указать функцию вызова, которая уведомляет о вызовах в рамках уведомления.  Функция callback соответствует [прототипу NOTIFCALLBACK.](notifcallback.md) Функции обратного вызова, реализованные клиентами, всегда возвращают S_OK; Функции обратного вызова, реализованные поставщиками служб, могут возвращать CALLBACK_DISCONTINUE. 
  
Если функция обратного вызова возвращает CALLBACK_DISCONTINUE, MAPI прекращает отправку уведомлений и NOTIFY_CANCELED в параметре _lpulFlags_ метода **Notify.** Можно предположить, что этот процесс неактивный, и прекратить создание уведомлений для этого процесса. Если **notify** возвращает 0 в  _lpulFlags,_ процесс по-прежнему активен, и вы должны продолжать отправлять уведомления, если это необходимо.
  
При использовании синхронных уведомлений будьте осторожны, чтобы избежать ситуаций с блокировкой.
  
Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md) 
  
## <a name="see-also"></a>См. также

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [�����������](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Каноническое свойство PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

