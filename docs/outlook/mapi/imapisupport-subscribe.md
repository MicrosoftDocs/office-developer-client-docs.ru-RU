---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419928"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует раковину рекомендации для получения уведомлений через MAPI.
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameters

 _lpKey_
  
> [in] Указатель на ключ уведомлений, который представляет исходный объект консультации. Параметр  _lpKey не_ может быть NULL. 
    
 _ulEventMask_
  
> [in] Маска значений, которые указывают типы событий уведомлений, которые интересуют вызываемого и должны быть включены в регистрацию. Допустимы следующие значения:
    
 _fnevCriticalError_
  
> Регистрирует уведомления о серьезных ошибках, например о недостаточной памяти.
    
 _fnevExtended_
  
> Регистрация уведомлений о событиях, определенных конкретному поставщику адресной книги или магазина сообщений.
    
 _fnevNewMail_
  
> Регистрация уведомлений о прибытии новых сообщений. 
    
 _fnevObjectCreated_
  
> Регистрирует уведомления о создании нового объекта.
    
 _fnevObjectCopied_
  
> Регистрация уведомлений о копировании объекта.
    
 _fnevObjectDeleted_
  
> Регистрация уведомлений об удалении объекта.
    
 _fnevObjectModified_
  
> Регистры уведомлений о модифицированном объекте.
    
 _fnevObjectMoved_
  
> Регистрация уведомлений о перемещении объекта.
    
 _fnevSearchComplete_
  
> Регистрация уведомлений о завершении операции поиска.
    
 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют, как происходит уведомление. Можно установить следующий флаг:
    
NOTIFY_SYNC 
  
> Когда звонящий вызывает [метод IMAPISupport::Notify](imapisupport-notify.md) для создания уведомлений для этой раковины **рекомендации,** Сообщите должны сделать все необходимые вызовы, чтобы проконсультировать раковины перед возвращением. Если этот флаг не установлен, уведомление является асинхронным, а вызовы вызовов в очереди на процессы, которые подписаны и запущены, когда эти процессы получают контроль над ЦП. 
    
 _lpAdviseSink_
  
> [in] Указатель на объект раковины рекомендации. 
    
 _lpulConnection_
  
> [вышел] Указатель на номер подключения незеро, который представляет регистрацию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений прошла успешно.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::Subscribe** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг **звонят Подписка** из одного из методов **консультирования,** чтобы разрешить MAPI управлять уведомлениями. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы использовать методы поддержки MAPI для уведомления, создайте ключ для источника консультаций объекта, о котором должны создаваться уведомления. Значение ключа должно быть уникальным и легко регенерироваться каждый раз, когда объект изменяется. 
  
MAPI использует ключ уведомления для поиска любых функций вызова, зарегистрированных через функцию [HrAllocAdviseSink](hrallocadvisesink.md) для соответствующего источника консультаций. Передай этот ключ **В IMAPISupport:::Notify,** когда необходимо создать уведомление для соответствующего источника консультаций. 
  
Флаг NOTIFY_SYNC влияет на работу последующих вызовов для **уведомления**. Когда вы NOTIFY_SYNC, **Уведомление** не возвращается, пока не завершит отправку всех необходимых уведомлений. Если вы не NOTIFY_SYNC, **уведомление** работает асинхронно, возможно, возвращается до всех уведомлений были отправлены. 
  
## <a name="see-also"></a>См. также



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�����������](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

