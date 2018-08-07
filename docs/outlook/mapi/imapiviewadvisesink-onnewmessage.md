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
ms.openlocfilehash: adf9b28e941e9ead9b83660f58701f13f35cabc7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809251"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**Относится к**: Outlook 
  
Уведомляет средство просмотра формы после загрузки, что новое или существующее сообщение в форме.
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Уведомление успешно завершен.
    
## <a name="remarks"></a>Замечания

Объекты формы вызовите метод **IMAPIViewAdviseSink::OnNewMessage** каждый раз, когда сообщение будет загружен в форму с помощью метода либо [IPersistMessage::InitNew](ipersistmessage-initnew.md) , либо [IPersistMessage::Load](ipersistmessage-load.md) . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Выпуск active указателя на объект формы, так как он больше не указывает на сообщение, которое ранее Просмотр используемого средства просмотра. 
  
Дополнительные сведения о уведомлений формы можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>См. также



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

