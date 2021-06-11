---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419606"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сообщает зрителю формы, что новое или существующее сообщение загружено в форме.
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно.
    
## <a name="remarks"></a>Примечания

Объекты форм называют метод **IMAPIViewAdviseSink::OnNewMessage** всякий раз, когда сообщение загружается в форме с помощью метода [IPersistMessage::InitNew](ipersistmessage-initnew.md) или [IPersistMessage::Load.](ipersistmessage-load.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Отпустите активный указатель к объекту формы, так как он больше не указывает на сообщение, которое ранее просматривал зритель. 
  
Дополнительные сведения об уведомлениях формы см. в рублях [Отправка и получение уведомлений о форме.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>См. также



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

