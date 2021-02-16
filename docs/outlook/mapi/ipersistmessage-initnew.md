---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317152"
---
# <a name="ipersistmessageinitnew"></a>IPersistMessage::InitNew

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Инициализирует новое сообщение.
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Параметры

 _pMessageSite_
  
> [in] Указатель на сайт сообщения, который форма будет использовать для работы с сообщением в просматриваемом объекте.
    
 _pMessage_
  
> [in] Указатель на новое сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новое сообщение было успешно инициализировано.
    
## <a name="remarks"></a>Примечания

Пользователи, которые могут вызывать метод **IPersistMessage::InitNew,** когда пользователь записывает новое сообщение, которое принадлежит классу сообщений, обрабатываемого формой. Если объект формы имеет допустимый указатель пользовательского интерфейса, должен отображаться пользовательский интерфейс для объекта сообщения. 
  
 **InitNew** не должен быть вызван, если форма находится в любом состоянии, кроме [неинициализированного](uninitialized-state.md) состояния. Если при вызвании **InitNew** форма находится в одном из других E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Как правило, сообщения с нес сохраненными свойствами помечают как измененные, чтобы клиент мог отобразить диалоговое окно с запросом о том, следует ли сохранить эти свойства. Если пользователь указывает, что сообщение должно быть сохранено, сохраните данные, пометите сообщение как чистое и выйдите из него в обычном режиме.
  
Однако если обработка только что инициализированных сообщений включает настройку одного или более вычисляемого свойства и важно сохранить эти свойства, не пометите сообщения как измененные. Так как вычисленные свойства должны быть невидимы для пользователей, диалоговое окно не должно отображаться.
  
Если форма имеет ссылку на активный сайт сообщений, который не передается в **InitNew,** отпустите исходный сайт, так как он больше не будет использоваться. Храните указатели на сайт сообщения и сообщение из параметров  _pMessageSite_ и  _pMessage,_ а также вызовите методы [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) обоих объектов, чтобы повысьть количество ссылок. 
  
**Задайте** свойства PR_MESSAGE_FLAGS ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)и **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)для нового сообщения на что-то, подходящее для вашего класса сообщения. Многие классы сообщений, например, **PR_MESSAGE_FLAGS** MSGFLAG_UNSENT для новых сообщений. 
  
Прежде чем возвращать форму, переходите в [обычное](normal-state.md) состояние, если ошибок не произошло. Отправьте новое уведомление всем зарегистрированным зрителям, вызывая их методы [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) и возвращая S_OK. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После успешного вызова **InitNew** можно предположить, что для формы задались следующие необходимые свойства, а не другие:
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)
  
 **PR_IMPORTANCE** ([PidTagImportance)](pidtagimportance-canonical-property.md)
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested)](pidtagoriginatordeliveryreportrequested-canonical-property.md)
  
 **PR_PRIORITY** ([PidTagPriority)](pidtagpriority-canonical-property.md)
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)
  
 **PR_SENSITIVITY** ([PidTagSensitivity)](pidtagsensitivity-canonical-property.md)
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId)](pidtagsentmailentryid-canonical-property.md)
  
Дополнительные сведения о состояниях форм см. в [сведениях о состояниях форм.](form-states.md) Дополнительные сведения об инициализации объектов хранилища см. в методе [IPersistStorage::InitNew.](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

