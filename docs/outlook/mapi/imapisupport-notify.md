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
ms.openlocfilehash: f79e5eaa3155bbe3373f5ad9c5182a4a65c62648
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572041"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Отправляет уведомление об указанном события источника уведомлений, изначально зарегистрированных для уведомления с помощью метода [IMAPISupport::Subscribe](imapisupport-subscribe.md) . 
  
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
  
> [in] Указатель на ключ уведомления для объекта источника уведомлений. Параметр _lpKey_ не может быть NULL. 
    
_cNotification_
  
> [in] Количество уведомлений структуры, на который указывает параметр _lpNotifications_ . 
    
_lpNotifications_
  
> [in] Указатель на массив структур [УВЕДОМЛЕНИЙ](notification.md) , которые описывают ожидающие уведомления. 
    
_lpulFlags_
  
> [in, out] Битовая маска флаги, который управляет процессом уведомления. Для ввода данных можно задать следующий флаг:
    
  - MAPI_UNICODE 
    
    > Строки в структур уведомлений, на который указывает _lpNotifications_ хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 

    На выходе MAPI можно задать следующий флаг:
        
  - NOTIFY_CANCELED 
    
    > Функция обратного вызова отменено синхронного уведомления.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Уведомления были успешно созданы.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::Notify** применяется для всех объектов поддержки поставщика службы. Поставщики услуг вызова **уведомления** для запроса, что MAPI создания уведомления для приемника уведомления, который ранее был зарегистрирован для уведомления через метод **IMAPISupport::Subscribe** . 
  
**Уведомлять** копии структур указывает параметр _lpNotifications_ в память и вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник соответствующих уведомлений. По завершении **OnNotify** с уведомлением освобождает используемые памяти. Вызывающий не нужно выделить память; MAPI выполняет все необходимые памяти. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Клавиша уведомлений, переданной в параметре _lpKey_ должен быть идентичен ключ, переданный в метод **IMAPISupport::Subscribe** _lpKey_ . Многие поставщики используется идентификатор записи источника уведомлений в качестве ключа, но можно использовать другие данные, такие как пути к файлу. MAPI использует этот ключ для поиска всех регистраций уведомлений на источник определенного уведомлений. 
  
Не забудьте установить член **lpEntryID** структуры уведомления для долгосрочного идентификатор записи. 
  
Если задать флаг NOTIFY_SYNC на **подписки на** звонок для каких-либо ожидающие уведомления **Уведомлять** звонки в функции обратного вызова метода **IMAPIAdviseSink::OnNotify** перед возвращением. Приемника уведомления могут создаваться вручную или посредством вызова [HrAllocAdviseSink](hrallocadvisesink.md). Функция **HrAllocAdviseSink** позволяет указать функции обратного вызова, звонки **Уведомлять** как часть уведомления, вызывающий. Если функция обратного вызова соответствует прототип [NOTIFCALLBACK](notifcallback.md) . Функции обратного вызова, реализуемый клиентами всегда возвращает значение S_OK; функции обратного вызова, реализованные поставщиков услуг может вернуть CALLBACK_DISCONTINUE. 
  
Если функция обратного вызова возвращает CALLBACK_DISCONTINUE, MAPI останавливает отправки уведомлений и возвращает NOTIFY_CANCELED в параметре _lpulFlags_ метод **уведомления** . Предполагается, что процесс неактивных и завершения создания уведомлений для этого процесса. Если **уведомление** возвращает 0 в _lpulFlags_, процесс по-прежнему активен и должны продолжать отправлять уведомления, соответствующим образом.
  
При использовании синхронного уведомления, будьте внимательны, чтобы избежать подобных ситуаций.
  
Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>См. также

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [�����������](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Каноническое свойство PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

