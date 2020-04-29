---
title: иперсистмессажеинитнев
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

 _пмессажесите_
  
> возврата Указатель на сайт сообщений, который форма будет использовать для работы с сообщением в средстве просмотра.
    
 _пмессаже_
  
> возврата Указатель на новое сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новое сообщение успешно инициализировано.
    
## <a name="remarks"></a>Примечания

Средства просмотра форм вызывают метод **иперсистмессаже:: инитнев** , когда пользователь записывает новое сообщение, принадлежащее классу сообщений, который обрабатывается формой. Если объект Form имеет допустимый указатель пользовательского интерфейса, необходимо отобразить пользовательский интерфейс для объекта Message. 
  
 **Инитнев** не следует вызывать, если форма находится в любом состоянии, кроме [неинициализированного](uninitialized-state.md) состояния. Если форма находится в одном из других состояний при вызове **инитнев** , возвращается E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Как правило, сообщения с несохраненными свойствами помечаются как измененные, чтобы клиент мог отобразить диалоговое окно, предлагающее пользователю указать, следует ли сохранять эти свойства. Если пользователь указывает, что необходимо сохранить сообщение, сохранить данные, пометить сообщение как чистый и выйти из него обычным способом.
  
Тем не менее, если при обработке новых инициализированных сообщений задано одно или несколько вычисляемых свойств, важно, чтобы эти свойства были сохранены, не помечать сообщения как измененные. Так как вычисляемые свойства должны быть невидимы для пользователей, диалоговое окно не должно отображаться.
  
Если форма содержит ссылку на активный сайт сообщений, отличный от переданного в **инитнев**, освободите исходный сайт, так как он больше не будет использоваться. Храните указатели на сайт сообщения и сообщение из параметров _пмессажесите_ и _пмессаже_ , а также вызывайте оба объекта: методы [AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) для увеличения счетчиков ссылок. 
  
Задайте свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) и **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) для нового сообщения, соответствующие классу сообщений. Многие классы сообщений, например, присвоить **PR_MESSAGE_FLAGS** MSGFLAG_UNSENT для новых сообщений. 
  
Прежде чем возвратить форму, переведите ее в [нормальное](normal-state.md) состояние, если ошибок не было. Отправьте новое уведомление всем зарегистрированным читателям, вызвав их методы [имапивиевадвисесинк:: онневмессаже](imapiviewadvisesink-onnewmessage.md) и возвращая S_OK. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После успешного вызова **инитнев**можно предположить, что для формы заданы следующие обязательные свойства, а не другие.
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Более подробную информацию о состояниях форм можно узнать в статье [состояния форм](form-states.md). Дополнительные сведения о том, как инициализируются объекты хранилища, можно найти в методе [иперсистстораже:: инитнев](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

