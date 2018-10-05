---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395940"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Загружает формы для указанного сообщения.
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>Параметры

 _pMessageSite_
  
> [in] Указатель на сообщение сайта для формы для загрузки.
    
 _pMessage_
  
> [in] Указатель на сообщение, для которого следует загрузить форму.
    
 _ulMessageStatus_
  
> [in] Битовая маска флагов клиента или поставщика, скопированные из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщение, предоставляют информацию о состоянии сообщения.
    
 _ulMessageFlags_
  
> [in] Битовая маска флагов, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщение, предоставляют информацию о состоянии сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма успешно загружен.
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IPersistMessage::Load** для загрузки формы для существующего сообщения. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

 **Нагрузки** вызывается только при открытии формы в одном из следующих состояний: 
  
- [Неинициализированная переменная](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Если форма просмотра вызывает **нагрузки** , пока форма находится в другое состояние, метод возвращает значение E_UNEXPECTED. 
  
Если форма имеет ссылку на сайт active сообщение помимо того, передаваемый в **нагрузки**, так как он больше не будет использоваться release исходного сайта. Хранение указатели на сайт сообщений и сообщений из параметров _pMessageSite_ и _pMessage_ и вызвать методы [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) оба объекта для увеличения их счетчики ссылок. 
  
После завершения **AddRef** хранилища свойств из параметров _ulMessageStatus_ и _ulMessageFlags_ в данный момент форму. Перенос форм в состояние [Normal](normal-state.md) перед их отображением и уведомить зарегистрированных средств просмотра, вызвав их [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) методы. 
  
При отсутствии ошибок возвращает значение S_OK. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Неинициализированное состояние](uninitialized-state.md)
  
[Состояние HandsOffAfterSave](handsoffaftersave-state.md)
  
[Состояние HandsOffFromNormal](handsofffromnormal-state.md)
  
[Состояния форм](form-states.md)


[IPersistStorage::Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream::Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile::Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

