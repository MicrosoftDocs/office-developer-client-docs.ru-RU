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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Инициализирует новое сообщение.
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parameters

 _pMessageSite_
  
> [in] Указатель на сайт сообщения, который форма будет использовать для работы с сообщением в просмотре.
    
 _pMessage_
  
> [in] Указатель на новое сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новое сообщение было успешно инициализировано.
    
## <a name="remarks"></a>Примечания

Зрители форм называют **метод IPersistMessage::InitNew,** когда пользователь пишет новое сообщение, которое относится к классу сообщений, который обрабатывает форма. Если объект формы имеет допустимый указатель пользовательского интерфейса, должен отображаться пользовательский интерфейс объекта сообщения. 
  
 **InitNew** не следует называть, если форма находится в любом состоянии, кроме [единого состояния.](uninitialized-state.md) Если форма находится в одном из других состояниях, когда **называется InitNew,** верните E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Как правило, сообщения, которые имеют неоплаченные свойства, помечены как измененные, чтобы клиент мог отображать диалоговое окно, которое подсказывает пользователю, следует ли сохранить эти свойства. Если пользователь указывает, что сообщение должно быть сохранено, сохраните данные, пометите сообщение как чистое и выйти в нормальном режиме.
  
Однако, если обработка новых инициализированных сообщений включает в себя установку одного или более вычислительных свойств, и это важно для этих свойств, которые необходимо сохранить, не пометите сообщения как измененные. Поскольку вычислительные свойства должны быть невидимыми для пользователей, диалоговое окно не должно отображаться.
  
Если ваша форма имеет ссылку на активный сайт сообщений, кроме того, который передается **в InitNew,** отпустите исходный сайт, так как он больше не будет использоваться. Храните указатели на сайте сообщений и сообщения из параметров  _pMessageSite_ и  _pMessage_ и вызывайте методы [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) для приумношения их отсчетов ссылок. 
  
Установите **свойства PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)и **PR_MSG_STATUS** [(PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)для нового сообщения на что-то подходящее для класса сообщений. Например, во многих классах сообщений **PR_MESSAGE_FLAGS** MSGFLAG_UNSENT для новых сообщений. 
  
Перед возвращением переоформить форму в [нормальное](normal-state.md) состояние, если ошибки не произошли. Отправьте новое уведомление всем зарегистрированным зрителям, позвонив по их методам [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) и S_OK. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После успешного вызова **в InitNew** можно предположить, что для формы установлены следующие необходимые свойства, а не другие:
  
 **PR_DELETE_AFTER_SUBMIT** [(PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)
  
 **PR_IMPORTANCE** [(PidTagImportance)](pidtagimportance-canonical-property.md)
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** [(PidTagOriginatorDeliveryReportReportRequested)](pidtagoriginatordeliveryreportrequested-canonical-property.md)
  
 **PR_PRIORITY** [(PidTagPriority)](pidtagpriority-canonical-property.md)
  
 **PR_READ_RECEIPT_REQUESTED** [(PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)
  
 **PR_SENSITIVITY** [(PidTagSensitivity)](pidtagsensitivity-canonical-property.md)
  
 **PR_SENTMAIL_ENTRYID** [(PidTagSentMailEntryId)](pidtagsentmailentryid-canonical-property.md)
  
Дополнительные сведения о состояниях форм см. в [дополнительных сведениях о состояниях форм.](form-states.md) Дополнительные сведения о том, как инициализировать объекты хранилища, см. в [методе IPersistStorage::InitNew.](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

