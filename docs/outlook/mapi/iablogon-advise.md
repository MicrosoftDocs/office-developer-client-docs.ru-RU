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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Регистрирует вызываемого пользователя для получения уведомлений об указанных событиях, влияющих на контейнер, пользователя обмена сообщениями или список рассылки.
  
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
  
> [in] Количествобайтов в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи объекта, о котором должны быть созданы уведомления.
    
 _ulEventMask_
  
> [in] Битоваяmas значений, которая указывает типы событий уведомлений, которые интересуют вызываемого и должны быть включены в регистрацию. Существует соответствующая структура [УВЕДОМЛЕНий,](notification.md) связанная с каждым типом события, который содержит сведения о событии. В следующей таблице перечислены допустимые значения для параметра  _ulEventMask_ и структуры, связанные с каждым значением. 
    
|**Тип события уведомления**|**Соответствующая **структура УВЕДОМЛЕНий****|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Указатель на объект приемника рекомендации для получения последующих уведомлений.
    
 _lpulConnection_
  
> [out] Указатель на неимякое значение, которое представляет регистрацию уведомлений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений прошла успешно.
    
MAPI_E_INVALID_ENTRYID 
  
> Идентификатор записи, переданный в  _параметре lpEntryID,_ не имеет соответствующего формата. 
    
MAPI_E_NO_SUPPORT 
  
> Поставщик адресной книги не поддерживает уведомление, возможно, потому, что он не позволяет вносить изменения в свои объекты.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Поставщик адресной книги не может обрабатывать идентификатор записи, переданный _в lpEntryID._
    
## <a name="remarks"></a>Примечания

Поставщики адресных книг реализуют метод **IABLogon::Advise** для регистрации вызываемого объекта для получения уведомлений при изменении объекта в одном из контейнеров. Звоняющие могут регистрироваться для уведомлений о пользователях сообщений, списках рассылки или целых контейнерах. 
  
Клиенты обычно звонят [методу IAddrBook::Advise](iaddrbook-advise.md) для регистрации уведомлений адресной книги. MAPI затем вызывает метод **Advise** поставщика адресной книги, который отвечает за объект, представленный идентификатором записи  _в lpEntryID_.
  
При изменении объекта, представленного в _ulEventMask,_ происходит вызов метода **OnNotify** приемника консультации, на который указывает _lpAdviseSink._ Данные, переданные в **структуре NOTIFICATION** процедуре **OnNotify,** описывают событие. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы можете поддерживать уведомления с помощью MAPI или без нее. MAPI имеет три метода объекта поддержки, которые помогают поставщикам услуг реализовать уведомления:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Если вы выбрали использование методов поддержки MAPI, вызовите **subscribe** при вызове метода **Advise** и отпустите указатель _lpAdviseSink._ 
  
Если вы самостоятельно выбрали поддержку уведомления, вызовите метод **AddRef** приемника рекомендации, представленного параметром  _lpAdviseSink,_ чтобы сохранить копию этого указателя. Сохраните эту копию, пока не будет вызван метод [IABLogon::Unadvise](iablogon-unadvise.md) для отмены регистрации. 
  
Независимо от того, как вы поддерживаете уведомление, назначьте ненулевую номер подключения регистрации уведомления и вернетесь в _параметре lpulConnection._ Не отпускать этот номер подключения, пока не будет вызван метод **Unadvise.** 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Указатель lpAdviseSink, переданный в параметр  _lpAdviseSink,_ может указать на созданный объект или на созданный с помощью функции [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) mapI. Вы можете использовать **HrThisThreadAdviseSink,** если поддерживаете несколько потоков выполнения и хотите убедиться, что последующие вызовы метода **OnNotify** происходят в соответствующее время в соответствующем потоке. 
  
Будьте готовы к тому, что ваш объект-тонконвейдер будет освобожден в любое время после вызова "Сообщить" и до вызова **unadvise.**  Следовательно, после возврата "Advise"  вам следует освободить объект-тонконсульт, если вы не используете его в течение длительного времени. 
  
Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md) Сведения об использовании методов **IMAPISupport** для поддержки уведомлений см. в подразделе ["Поддержка уведомлений о событиях".](supporting-event-notification.md) Дополнительные сведения о многопотооке и MAPI см. в [threading in MAPI.](threading-in-mapi.md)
  
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�����������](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

