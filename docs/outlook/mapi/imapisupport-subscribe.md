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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Регистрирует приемник уведомлений для получения уведомлений через MAPI.
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Параметры

 _lpKey_
  
> [in] Указатель на ключ уведомления, который представляет исходный объект консультации. Параметр  _lpKey не может_ иметь NULL. 
    
 _ulEventMask_
  
> [in] Маска значений, которые указывают типы событий уведомлений, которые интересуют вызываемого и должны быть включены в регистрацию. Допустимы следующие значения:
    
 _fnevCriticalError_
  
> Регистрирует уведомления о серьезных ошибках, например нехватке памяти.
    
 _fnevExtended_
  
> Регистрируется для уведомлений о событиях, характерных для конкретной адресной книги или поставщика store сообщений.
    
 _fnevNewMail_
  
> Регистрируется для уведомлений о поступлении новых сообщений. 
    
 _fnevObjectCreated_
  
> Регистрируется для уведомлений о создании нового объекта.
    
 _fnevObjectCopied_
  
> Регистрируется для уведомлений об объекте, который копируется.
    
 _fnevObjectDeleted_
  
> Регистрирует уведомления об удаляемом объекте.
    
 _fnevObjectModified_
  
> Регистрирует уведомления об изменяемом объекте.
    
 _fnevObjectMoved_
  
> Регистрирует уведомления о перемещаемом объекте.
    
 _fnevSearchComplete_
  
> Регистрируется для уведомлений о завершении операции поиска.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет процессом уведомления. Можно установить следующий флаг:
    
NOTIFY_SYNC 
  
> Когда звонящий вызывает метод [IMAPISupport::Notify](imapisupport-notify.md) для создания уведомлений для этого приемника с **консультацией,** перед возвратом необходимо уведомить его о всех необходимых вызовах, чтобы сообщить приемникам. Если этот флаг не установлен, уведомление является асинхронным, а перезаписи вызовов находятся в очереди к процессам, которые подписаны и запущены, когда эти процессы получают контроль над ЦП. 
    
 _lpAdviseSink_
  
> [in] Указатель на объект-тонущий объект консультации. 
    
 _lpulConnection_
  
> [out] Указатель на номер подключения, который не является номером для регистрации.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений прошла успешно.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::Subscribe** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг **звонят подписку** из одного из своих методов **advise,** чтобы разрешить MAPI управлять уведомлениями. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы использовать методы поддержки MAPI для уведомлений, создайте ключ для источника консультации, в котором будет создан объект, о котором должны создаваться уведомления. Значение ключа должно быть уникальным и легко регенерироваться при каждом смене объекта. 
  
MAPI использует ключ уведомления для поиска любых функций, зарегистрированных с помощью функции [HrAllocAdviseSink](hrallocadvisesink.md) для соответствующего источника консультации. Передайте этот ключ **в IMAPISupport::Notify,** если вам нужно создать уведомление для соответствующего источника консультации. 
  
Флаг NOTIFY_SYNC влияет на работу последующих вызовов **notify**. Если вы NOTIFY_SYNC, **notify** не возвращается, пока не завершит отправку всех необходимых уведомлений. Если вы не NOTIFY_SYNC, **уведомление** работает асинхронно, возможно, возвращается до того, как будут отправлены все уведомления. 
  
## <a name="see-also"></a>См. также



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�����������](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

