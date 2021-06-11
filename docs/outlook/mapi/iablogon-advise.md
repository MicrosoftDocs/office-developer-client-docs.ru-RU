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
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428230"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует вызываемого пользователя для получения уведомления о указанных событиях, затрагивающих контейнер, пользователя обмена сообщениями или список рассылки.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Количество bytes в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор входа объекта, о котором должны быть созданы уведомления.
    
 _ulEventMask_
  
> [in] Битмаска значений, которые указывают типы событий уведомлений, которые вызываемого заинтересована и должна быть включена в регистрацию. Существует соответствующая структура [УВЕДОМЛЕНий,](notification.md) связанная с каждым типом события, которое содержит сведения о событии. В следующей таблице перечислены допустимые значения для  _параметра ulEventMask_ и структуры, связанные с каждым значением. 
    
|**Тип события уведомлений**|**Соответствующая **структура УВЕДОМЛЕНий****|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Указатель на объект раковины для получения последующих уведомлений.
    
 _lpulConnection_
  
> [вышел] Указатель на значение nonzero, представляю которое представляет регистрацию уведомлений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений прошла успешно.
    
MAPI_E_INVALID_ENTRYID 
  
> Идентификатор записи, переданный в  _параметре lpEntryID,_ не находится в соответствующем формате. 
    
MAPI_E_NO_SUPPORT 
  
> Поставщик адресной книги не поддерживает уведомление, возможно, потому, что оно не позволяет вносить изменения в свои объекты.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Поставщик адресной книги не может обрабатывать идентификатор записи, переданный _в lpEntryID._
    
## <a name="remarks"></a>Примечания

Поставщики адресных книг реализуют метод **IABLogon::Advise,** чтобы зарегистрировать вызываемого для уведомления при изменении объекта в одном из контейнеров. Звонители могут регистрироваться для уведомлений о пользователях обмена сообщениями, списках рассылки или целых контейнерах. 
  
Клиенты обычно звонят по [методу IAddrBook::Advise](iaddrbook-advise.md) для регистрации уведомлений адресной книги. ЗАТЕМ MAPI вызывает метод **Advise** поставщика адресной книги, который отвечает за объект, представленный идентификатором записи _в lpEntryID._
  
При изменении указанного объекта типа, представленного в  _ulEventMask,_ в метод **OnNotify** в раковине рекомендации  _указывается lpAdviseSink_. Данные, переданные в **структуре УВЕДОМЛЕНий** в **рутину OnNotify,** описывают событие. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы можете поддерживать уведомление с помощью MAPI или без нее. MAPI имеет три метода объектов поддержки, которые помогают поставщикам услуг реализовать уведомление:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Если вы хотите использовать методы поддержки  MAPI,  позвоните подписаться при вызове метода Advise и отпустите указатель _lpAdviseSink._ 
  
Если вы сами хотите поддержать уведомление, позвоните **методу AddRef** раковины рекомендации, представленной параметром  _lpAdviseSink,_ чтобы сохранить копию этого указателя. Сохраните эту копию, пока не будет вызван метод [IABLogon::Unadvise](iablogon-unadvise.md) для отмены регистрации. 
  
Независимо от того, как вы поддерживаете уведомление, назначьте номер подключения, неподключаемого к уведомлению, и верни его в _параметре lpulConnection._ Не отпустите этот номер подключения до тех пор, пока не будет вызван метод **Unadvise.** 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Указатель на раковину, который вы передаете в _параметре lpAdviseSink,_ может указать на объект, созданный вами или созданный MAPI с помощью функции [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md)  Возможно, вы захотите использовать **HrThisThreadAdviseSink,** если поддерживаете несколько потоков выполнения и хотите убедиться, что последующие вызовы в метод **OnNotify** происходят в соответствующее время в соответствующем потоке. 
  
Будьте готовы к тому, что объект раковины  рекомендации будет выпущен в любое время после звонка в Совет и перед вызовом **в Unadvise.** Поэтому после возврата рекомендации следует освободить  объект погрузки, если для этого не будет определенного долгосрочного использования. 
  
Дополнительные сведения о процессе уведомления см. в сообщении [события в MAPI.](event-notification-in-mapi.md) Сведения о том, как использовать методы **IMAPISupport** для поддержки уведомления, см. в сообщении [о поддержке событий.](supporting-event-notification.md) Дополнительные сведения о многопотоковом и MAPI см. в [ведомости в MAPI.](threading-in-mapi.md)
  
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�����������](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

