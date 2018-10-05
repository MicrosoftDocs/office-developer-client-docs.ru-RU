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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394883"
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
  
> [in] Указатель на сайте сообщения, форма будет использоваться для работы с сообщением в средстве просмотра.
    
 _pMessage_
  
> [in] Указатель на новое сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новое сообщение успешно инициализирована.
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IPersistMessage::InitNew** при записи нового сообщения, к которой принадлежит класс сообщений, который обрабатывает формы пользователем. Если объект формы указатель интерфейса пользователя, должно отображаться пользовательского интерфейса для объекта сообщения. 
  
 **InitNew** не должен вызываться, когда формы — в любом состоянии, кроме состояния [не инициализировано](uninitialized-state.md) . Если форма находится в одном из других состояний при вызове **InitNew** , возвратите значение E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Как правило сообщения, которые имеются несохраненные свойства помечаются как измененные, чтобы клиент может отображать диалоговое окно, в котором пользователь должен быть сохранен этих свойств. Если пользователь указывает, сохранить сообщение, сохранить данные, пометить сообщение как чистая и выйдите из обычно.
  
Тем не менее если обработки вновь инициализированный сообщений включает в себя определения значения для одного или нескольких вычисляемых свойств и очень важно для этих свойств для сохранения, помечает сообщения как изменены. Так как вычисляемые свойства должны быть невидимы для пользователей, диалоговое окно не должно отображаться.
  
Если форма имеет ссылку на сайт active сообщение помимо того, передаваемый в **InitNew**, release исходного сайта, так как он больше не будет использоваться. Хранение указатели на сайт сообщений и сообщений из параметров _pMessageSite_ и _pMessage_ и вызвать методы [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) оба объекта для увеличения их счетчики ссылок. 
  
Настройка параметров **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) и **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) для нового сообщения на что-то соответствующий класс сообщения. Множество классов сообщений, например, значение **PR_MESSAGE_FLAGS** MSGFLAG_UNSENT для новых сообщений. 
  
До возвращения происходили перехода формы в состояние [Normal](normal-state.md) Если без ошибок. Отправлять уведомление о получении сообщений всем зарегистрированным пользователям, вызвав их методы [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) и возвращает значение S_OK. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После успешного вызова **InitNew**предполагается, что следующие обязательные свойства и другие, заданные для формы:
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Дополнительные сведения о состояниях форм можно [Состояния формы](form-states.md). Дополнительные сведения о способ инициализации объектов хранилища [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) см. 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

