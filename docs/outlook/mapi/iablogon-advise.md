---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 926fef0e1b2f905d510102e69afb667414e6cce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808732"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Относится к**: Outlook 
  
Регистрирует вызывающего абонента для получения уведомлений о указанного события, которые влияют на container, системы обмена сообщениями пользователя или список рассылки.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Число байт в идентификаторе запись указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи о том, какие следует создавать уведомления объекта.
    
 _ulEventMask_
  
> [in] Битовая маска значений, которые указывают на тип события уведомлений, вызывающего заинтересована в и должно быть включено в регистрации. Нет соответствующих структура [уведомления](notification.md) , связанные с каждым типом событий, в котором содержатся сведения о событии. В следующей таблице приведены допустимые значения для параметра _ulEventMask_ и структуры, связанных с каждой значение. 
    
|**Тип события уведомления**|**Структура соответствующего **уведомления****|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Указатель на объект приемника уведомлений для последующих уведомлений.
    
 _lpulConnection_
  
> [out] Указатель на ненулевое значение, представляющее регистрации уведомлений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Уведомление о регистрации прошла успешно.
    
MAPI_E_INVALID_ENTRYID 
  
> Идентификатор записи, переданной в параметре _lpEntryID_ не находится в соответствующем формате. 
    
MAPI_E_NO_SUPPORT 
  
> Поставщик адресной книги не поддерживает уведомления, возможно, поскольку не позволяет вносить изменения в объекты.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Поставщик адресной книги не может обработать идентификатор записи, переданные в _lpEntryID_.
    
## <a name="remarks"></a>Замечания

Метод **IABLogon::Advise** для регистрации звонящего на получение уведомлений при изменении объект в одну из своих контейнеров, реализуемые поставщиками адресных книг. Вызывающие объекты можно регистрировать для уведомлений о обмена мгновенными сообщениями пользователи, списков рассылки или всей контейнеров. 
  
Клиенты обычно вызов метода [IAddrBook::Advise](iaddrbook-advise.md) для регистрации уведомлений адресной книги. MAPI вызывает метод **уведомлений** поставщик адресной книги, который несет ответственность за объекта, представленного идентификатор записи в _lpEntryID_.
  
При изменении на указанный объект типа, представленного в _ulEventMask_, выполняется вызов метода **OnNotify** приемник уведомлений, на который указывает _lpAdviseSink_. Данные, передаваемые в структуре **УВЕДОМЛЕНИЙ** в подпрограмму **OnNotify** описание события. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Может поддерживать уведомлений с помощью или без помощи MAPI. MAPI имеет поддержки объект методы, позволяющие реализовать уведомление поставщиков услуг:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Если вы решите использовать методы поддержки MAPI, вызовите **подписки на** при вызове метода **уведомлений** и освобождать указатель _lpAdviseSink_ . 
  
Если для поддержки уведомлений самостоятельно, вызовите метод **AddRef** приемник уведомлений, представленное параметром _lpAdviseSink_ сохранить копию этого указателя. Ведение эту копию, пока не будет вызван метод [IABLogon::Unadvise](iablogon-unadvise.md) для отмены регистрации. 
  
Независимо от того, как вы поддерживаете уведомлений нумерации ненулевое подключения для регистрации уведомлений и вернуть его в параметре _lpulConnection_ . Не release этот номер подключения до вызова метода **Unadvise** . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Объект, которые были созданы или создания MAPI через функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) можно сопоставить указателя приемника уведомлений, передаваемый в параметре _lpAdviseSink_ **уведомлений** . Можно использовать **HrThisThreadAdviseSink** , если поддержка нескольких потоков выполнения и хотите убедитесь, что последующие вызовы метода **OnNotify** возникают в соответствующее время на соответствующий поток. 
  
Подготовить для объекта приемник уведомлений нужно освободить любое время после вызова для **уведомлений** и до обращения к **Unadvise**. Таким образом необходимо разблокировать объект приемника уведомлений после возвращает **уведомлений** при отсутствии определенных длительного использования для него. 
  
Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md). Сведения о том, как использовать методы **IMAPISupport** для поддержки уведомлений [Поддержка уведомлений о событиях](supporting-event-notification.md)см. Дополнительные сведения о многопоточность и MAPI, видеть [Threading в MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�����������](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

