---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406278"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Регистрирует клиента или поставщика услуг для получения уведомлений об изменениях одной или более записей в адресной книге.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи контейнера адресной книги, пользователя системы обмена сообщениями или списка рассылки, который создает уведомление при изменении типа или типов, описанных в параметре _ulEventMask._ 
    
 _ulEventMask_
  
> [in] Одно или несколько событий уведомлений, которые звоняющий регистрирует для получения. Каждое событие связано с определенной структурой уведомлений, которая содержит сведения о произошедших изменениях. В следующей таблице перечислены допустимые значения  _для ulEventMask_ и соответствующих структур. 
    
|**Событие уведомления**|**Соответствующая структура**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Указатель на объект-консультант, который будет вызван при событии, для которого было запрощено уведомление.
    
 _lpulConnection_
  
> [out] Указатель на номер подключения, который представляет регистрацию уведомления.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений прошла успешно.
    
MAPI_E_INVALID_ENTRYID 
  
> Поставщику адресной книги, ответственному за идентификатор записи, переданный  _в lpEntryID,_ не удалось зарегистрировать уведомление для соответствующей записи. 
    
MAPI_E_NO_SUPPORT 
  
> Поставщик адресной книги, ответственный за объект, определяемой идентификатором записи, переданным в  _параметре lpEntryID,_ не поддерживает уведомление. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Идентификатор записи, переданный  _в lpEntryID,_ не может быть обработан ни одним из поставщиков адресной книги в профиле. 
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг звонят **методу Advise** для регистрации определенного типа или типов уведомлений в записи адресной книги. Типы уведомлений указываются маской события, передаемой с помощью параметра _ulEventMask._ 
  
MAPI передает этот вызов **advise** поставщику адресной книги, который отвечает за запись, указанную идентификатором записи в параметре _lpEntryID._ Поставщик адресной книги либо сам обрабатывает регистрацию, либо вызывает метод поддержки [IMAPISupport::Subscribe,](imapisupport-subscribe.md)чтобы указать MAPI зарегистрировать вызываемого. Возвращается номер подключения, который не является номером для успешной регистрации.
  
При изменении записи типа, указанного регистрацией уведомления, поставщик адресной книги вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемника рекомендации, указанного в параметре _lpAdviseSink._ Метод **OnNotify** включает структуру [NOTIFICATION](notification.md) в качестве входного параметра, который содержит данные для описания события. 
  
В зависимости от поставщика адресной книги вызов **OnNotify** может происходить сразу после изменения зарегистрированного объекта или позднее. В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** может происходить в любом потоке. Клиенты могут запрашивать эти уведомления в определенном потоке, вызывая функцию [HrThisThreadAdviseSink,](hrthisthreadadvisesink.md) чтобы создать объект-замещение, переданный в "Консультацию".  
  
Так как поставщик адресной книги может освободить объект-источник уведомлений, переданный клиентами, в любое время после успешного завершения вызова advise и перед вызовом  [IAddrBook::Unadvise,](iaddrbook-unadvise.md) чтобы отменить уведомление, клиенты должны освободить свои объекты-сигнальные сигналы, когда возвращается уведомление.  
  
Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md)
  
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�����������](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

