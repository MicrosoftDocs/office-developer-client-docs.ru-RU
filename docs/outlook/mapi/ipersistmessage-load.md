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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317131"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Загружает форму для указанного сообщения.
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>Parameters

 _pMessageSite_
  
> [in] Указатель на сайт сообщения для загрузки формы.
    
 _pMessage_
  
> [in] Указатель на сообщение, для которого должна быть загружена форма.
    
 _ulMessageStatus_
  
> [in] Битмаска флагов, определенных клиентом или поставщика, скопированная  из свойства PR_MSG_STATUS сообщения[(PidTagMessageStatus),](pidtagmessagestatus-canonical-property.md)которые предоставляют сведения о состоянии сообщения.
    
 _ulMessageFlags_
  
> [in] Битмашка флагов, скопированная из свойства[PR_MESSAGE_FLAGS (PidTagMessageFlags),](pidtagmessageflags-canonical-property.md)которые предоставляют дополнительные сведения о состоянии сообщения. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма была успешно загружена.
    
## <a name="remarks"></a>Примечания

Зрители форм называют **метод IPersistMessage::Load** для загрузки формы для существующего сообщения. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

 **Нагрузка** вызвана только в том случае, если форма находится в одном из следующих штатов: 
  
- [Uninitialized](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Если зритель формы вызывает **Load,** пока форма находится в любом другом состоянии, метод возвращается E_UNEXPECTED. 
  
Если ваша форма имеет ссылку на активный сайт сообщений, который не передается в **Load,** отпустите исходный сайт, так как он больше не будет использоваться. Храните указатели на сайте сообщений и сообщения из параметров  _pMessageSite_ и  _pMessage_ и вызывайте методы [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) для приумношения их отсчетов ссылок. 
  
После **завершения AddRef** храните свойства  _ulMessageStatus_ и  _ulMessageFlags_ в форму. Перед ее отображением перенаправляем форму в нормальное состояние и уведомляем зарегистрированных зрителей, вызывая их методы [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md) [](normal-state.md) 
  
Если ошибки не происходят, S_OK. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Единое состояние](uninitialized-state.md)
  
[Состояние HandsOffAfterSave](handsoffaftersave-state.md)
  
[HandsOffFromNormal State](handsofffromnormal-state.md)
  
[Состояния форм](form-states.md)


[IPersistStorage::Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream::Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile::Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

