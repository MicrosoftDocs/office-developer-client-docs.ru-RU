---
title: иперсистмессажелоад
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Загружает форму для указанного сообщения.
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>Параметры

 _пмессажесите_
  
> возврата Указатель на сайт сообщений для загружаемой формы.
    
 _пмессаже_
  
> возврата Указатель на сообщение, для которого должна быть загружена форма.
    
 _улмессажестатус_
  
> возврата Битовая маска определяемых клиентом или поставщика флагов, скопированная из свойства **PR_MSG_STATUS** сообщения ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)), которые предоставляют сведения о состоянии сообщения.
    
 _улмессажефлагс_
  
> возврата Битовая маска флагов, скопированных из свойства **PR_MESSAGE_FLAGS** сообщения ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)), которые предоставляют дополнительные сведения о состоянии сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма успешно загружена.
    
## <a name="remarks"></a>Примечания

Средства просмотра форм вызывают метод **иперсистмессаже:: Load** для загрузки формы для существующего сообщения. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

 Метод **Load** вызывается только в том случае, если форма находится в одном из следующих состояний: 
  
- [Неинициализированное](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Если средство просмотра формы вызывает **загрузку** , когда форма находится в любом другом состоянии, метод возвращает E_UNEXPECTED. 
  
Если форма содержит ссылку на активный сайт сообщений, отличную от переданной в **загрузку**, освободите исходный сайт, так как он больше не будет использоваться. Храните указатели на сайт сообщения и сообщение из параметров _пмессажесите_ и _пмессаже_ , а также вызывайте оба объекта: методы [AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) для увеличения счетчиков ссылок. 
  
После завершения **AddRef** сохраните свойства из параметров _улмессажестатус_ и _улмессажефлагс_ в форме. Перед отображением формы переведите ее в [нормальное](normal-state.md) состояние и уведомите зарегистрированных средств просмотра, вызвав их методы [Имапивиевадвисесинк:: онневмессаже](imapiviewadvisesink-onnewmessage.md) . 
  
Если ошибок не возникло, возвращается S_OK. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Неинициализированное состояние](uninitialized-state.md)
  
[Состояние HandsOffAfterSave](handsoffaftersave-state.md)
  
[Состояние HandsOffFromNormal](handsofffromnormal-state.md)
  
[Состояния форм](form-states.md)


[Иперсистстораже:: Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream:: Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile:: Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

