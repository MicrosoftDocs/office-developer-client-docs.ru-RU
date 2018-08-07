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
ms.openlocfilehash: 8214390af883432d72f608452b8b944417884fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808751"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**Относится к**: Outlook 
  
Регистрация клиента или поставщика для получения уведомлений об изменениях в одну или несколько записей в адресной книге.
  
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
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи контейнер адресной книги, системы обмена сообщениями пользователя или список рассылки, который будет создаваться уведомление, когда происходит изменение типа или типов, описанных в параметре _ulEventMask_ . 
    
 _ulEventMask_
  
> [in] Одно или несколько событий уведомлений, которые регистрации вызывающего абонента для получения. Каждое событие связан со структурой уведомление, который содержит сведения об изменениях, которые произошли. В следующей таблице перечислены допустимые значения для _ulEventMask_ и их соответствующие структуры. 
    
|**Уведомление о событии**|**Соответствующий структуры**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Указатель на элемент уведомлений приемник, который будет вызываться, когда происходит событие, для которого был запрошен уведомлений.
    
 _lpulConnection_
  
> [out] Указатель на подключение ненулевое число, представляющее регистрации уведомлений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Уведомление о регистрации прошла успешно.
    
MAPI_E_INVALID_ENTRYID 
  
> Поставщик адресной книги, ответственный за запись идентификатора, переданного в _lpEntryID_ не удалось зарегистрировать уведомления для соответствующей операции. 
    
MAPI_E_NO_SUPPORT 
  
> Уведомление не поддерживается поставщик адресной книги, ответственный за запись идентификатором, переданной в параметре _lpEntryID_ объекта. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Идентификатор записи, переданные в _lpEntryID_ не может справиться с любой из поставщиками адресной книги в профиле. 
    
## <a name="remarks"></a>Замечания

Клиенты и поставщики услуг вызовите метод **уведомлений** для регистрации для определенного типа или типов уведомлений на запись адресной книги. Типы уведомлений обозначены маска событие, переданное с помощью параметра _ulEventMask_ . 
  
MAPI переадресует этот вызов **уведомлений** для доступа к адресной книге, который несет ответственность за запись, что указывает идентификатор записи в параметре _lpEntryID_ . Поставщик адресной книги обрабатывает регистрации самого или вызывает метод поддержки [IMAPISupport::Subscribe](imapisupport-subscribe.md), чтобы запрашивать MAPI для регистрации вызывающего абонента. Для представления успешной регистрации возвращается число ненулевое подключения.
  
При каждом изменении записи тип, указанный в параметре регистрации уведомлений, поставщик адресной книги вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемник уведомлений, указанный в параметре _lpAdviseSink_ . Метод **OnNotify** содержит структуру [УВЕДОМЛЕНИЙ](notification.md) в качестве входного параметра, который содержит данные для описания события. 
  
В зависимости от доступа к адресной книге вызов **OnNotify** может произойти сразу после изменения зарегистрированных объект или позже. На компьютерах, поддерживающих многопоточной среде вызов **OnNotify** может выполняться на любой поток. Клиенты могут запрашивать только такие уведомления на определенного потока с помощью вызова функции [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) для создания объекта приемник уведомлений, который передается в **уведомлений**. 
  
Так как поставщика адресных книг можно освободить объект приемника уведомлений, переданного с клиентами в любое время после успешного завершения **уведомлений** звонков и перед [IAddrBook::Unadvise](iaddrbook-unadvise.md) звонок, чтобы отменить уведомление, освобождать клиентов их уведомлений приемника объектов при возврате **уведомлений** . 
  
Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�����������](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

