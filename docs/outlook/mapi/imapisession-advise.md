---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419837"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрируется для получения уведомления о указанных событиях, влияющих на сеанс.
  
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
  
> [in] Указатель на идентификатор записи объекта адресной книги или магазина сообщений о том, какие уведомления должны быть созданы, или NULL, который указывает, что клиент регистрируется для получения уведомлений о событиях, затрагивающих только сеанс. 
    
 _ulEventMask_
  
> [in] Маска значений, которые указывают типы событий уведомлений, которые интересуют клиента и должны быть включены в регистрацию. Если  _lpEntryID_ является NULL, MAPI автоматически регистрирует клиента для событий критической ошибки, которые влияют только на сеанс. Если  _lpEntryID_ указывает на идентификатор записи, для  _параметра ulEventMask_ допустимы следующие значения: 
    
fnevCriticalError 
  
> Регистрирует уведомления о серьезных ошибках, например о недостаточной памяти.
    
fnevExtended 
  
> Регистрирует уведомления о событиях, определенных конкретному поставщику адресной книги или магазина сообщений, а также о закрытии сеанса.
    
fnevNewMail 
  
> Регистрация уведомлений о прибытии новых сообщений. 
    
fnevObjectCreated 
  
> Регистрирует уведомления о создании нового объекта.
    
fnevObjectCopied
  
> Регистрация уведомлений о копировании объекта.
    
fnevObjectDeleted
  
> Регистрация уведомлений об удалении объекта.
    
fnevObjectModified
  
> Регистры уведомлений о модифицированном объекте.
    
fnevObjectMoved
  
> Регистрация уведомлений о перемещении объекта.
    
fnevSearchComplete
  
> Регистрация уведомлений о завершении операции поиска.
    
 _lpAdviseSink_
  
> [in] Указатель на объект раковины для получения последующих уведомлений. Этот объект по рекомендации должен быть уже выделен.
    
 _lpulConnection_
  
> [вышел] Указатель на номер nonzero, представляющий связь между объектом раковины рекомендации вызываемого звонищего и сеансом.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация прошла успешно.
    
MAPI_E_INVALID_ENTRYID 
  
> Идентификатор записи, на который указывает  _lpEntryID,_ не представляет допустимый идентификатор записи. 
    
MAPI_E_NO_SUPPORT 
  
> Поставщик услуг, отвечающий за идентификатор входа, на который указывает  _lpEntryID,_ либо не поддерживает тип событий, указанных в параметре  _ulEventMask,_ либо не поддерживает уведомление. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Идентификатор записи, на который указывает  _lpEntryID,_ не может обрабатываться любым из поставщиков услуг в профиле. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::Advise** устанавливает связь между объектом раковины рекомендации вызываемого, сеансом и, необязательно, поставщиком услуг. Это подключение используется для отправки уведомлений в раковину рекомендации, когда одно или несколько событий, указанных в параметре _ulEventMask,_ происходят с объектом, на который указывает _lpEntryID._ Если  _lpEntryID_ является NULL, целевым объектом является сеанс, и уведомления отправляются только для критических ошибок и расширенных событий. 
  
Когда _lpEntryID_ указывает на допустимый идентификатор  входа, MAPI вызывает метод Advise объекта logon, который принадлежит ответственному поставщику услуг. Например, если  _lpEntryID_ указывает на идентификатор записи списка рассылки, MAPI вызывает метод [IABLogon::Advise](iablogon-advise.md) соответствующего поставщика адресной книги. 
  
Чтобы отправить уведомление, поставщик услуг или MAPI вызывает зарегистрированный метод [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md) Один из параметров **OnNotify**, структуры уведомлений, содержит сведения, описывая конкретное событие.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** также может происходить в любом потоке в любое время. Если вам нужна уверенность в том, что уведомления будут возникать только в определенное время в определенном потоке, позвоните в функцию [HrThisThreadAdviseSink,](hrthisthreadadvisesink.md) чтобы создать объект-раковину, который вы передаете методу **Advise.** 
  
Чтобы определить, когда клиент отключается, зарегистрируйтесь для  уведомлений в поставщике услуг, позвонив в службу Консультирование с набором _lpEntryID_ в NULL и _cbEntryID,_ заданным до 0. Когда происходит вход, вы получите уведомление fnevExtended. 
  
После успешного  звонка в совет и до вызова [IMAPISession::Unadvise](imapisession-unadvise.md) для отмены регистрации отпустите объект раковины рекомендации, если для этого не будет определенного долгосрочного использования. 
  
Обзор процесса уведомлений см. в [примере Event Notification in MAPI.](event-notification-in-mapi.md) 
  
Дополнительные сведения об обработке уведомлений см. в [сообщении Handling Notifications.](handling-notifications.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI использует **метод IMAPISession::Advise** для регистрации уведомлений о сеансе.  <br/> |
   
## <a name="see-also"></a>См. также



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Уведомление о событиях в MAPI](event-notification-in-mapi.md)

