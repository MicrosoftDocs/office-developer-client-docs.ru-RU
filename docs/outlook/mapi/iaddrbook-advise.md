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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор входа контейнера адресной книги, пользователя обмена сообщениями или списка рассылки, который генерирует уведомление при изменении типа или типов, описанных в параметре _ulEventMask._ 
    
 _ulEventMask_
  
> [in] Одно или несколько событий уведомления, которые регистрируется для получения вызываемой стороны. Каждое событие связано с определенной структурой уведомлений, которая содержит сведения о произошедших изменениях. В следующей таблице перечислены допустимые значения  _для ulEventMask_ и их соответствующих структур. 
    
|**Событие уведомлений**|**Соответствующая структура**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Указатель на объект раковины рекомендации, который будет вызван, когда происходит событие, для которого было запрощено уведомление.
    
 _lpulConnection_
  
> [вышел] Указатель на номер подключения, который представляет регистрацию уведомлений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений прошла успешно.
    
MAPI_E_INVALID_ENTRYID 
  
> Поставщик адресной книги, ответственный за идентификатор записи, переданный  _в lpEntryID,_ не смог зарегистрировать уведомление для соответствующей записи. 
    
MAPI_E_NO_SUPPORT 
  
> Уведомление не поддерживается поставщиком адресной книги, ответственным за объект, идентифицированный идентификатором записи, переданным в _параметре lpEntryID._ 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Идентификатор записи, переданный  _в lpEntryID,_ не может обрабатываться любым из поставщиков адресных книг в профиле. 
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг звонят **методу Advise** для регистрации для определенного типа или типов уведомлений в записи адресной книги. Типы уведомлений указываются в маске события, переданной с _параметром ulEventMask._ 
  
MAPI передает этот вызов **сообщить** поставщику адресной книги, который отвечает за запись, как указано идентификатором записи в _параметре lpEntryID._ Поставщик адресной книги либо обрабатывает сам процесс регистрации, либо вызывает метод поддержки [IMAPISupport::Subscribe,](imapisupport-subscribe.md)чтобы побудить MAPI зарегистрировать вызываемого. Для успешной регистрации возвращается номер подключения незеро.
  
Всякий раз, когда происходит изменение в записи типа, указанного в регистрации уведомлений, поставщик адресной книги вызывает [метод IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта раковины рекомендации, указанного в параметре _lpAdviseSink._ Метод **OnNotify** включает структуру [УВЕДОМЛЕНий](notification.md) в качестве параметра ввода, который содержит данные для описания события. 
  
В зависимости от поставщика адресной книги вызов **OnNotify** может произойти сразу после изменения зарегистрированного объекта или позднее. В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** может происходить в любом потоке. Клиенты могут запросить, чтобы эти уведомления были в определенном потоке, позвонив в функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) для создания объекта-раковины, передаваемого **совету**. 
  
Так как поставщик адресной книги может освободить объект раковины рекомендации, переданный  клиентами в любое время после успешного завершения вызова "Советы" и перед вызовом  [IAddrBook::Unadvise,](iaddrbook-unadvise.md) чтобы отменить уведомление, клиенты должны освободить свои объекты раковины рекомендации, когда сообщите возвращается. 
  
Дополнительные сведения о процессе уведомления см. в сообщении [события в MAPI.](event-notification-in-mapi.md)
  
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�����������](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

