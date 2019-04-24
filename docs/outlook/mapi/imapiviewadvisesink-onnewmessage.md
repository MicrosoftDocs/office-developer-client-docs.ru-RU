---
title: Имапивиевадвисесинконневмессаже
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328793"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Уведомляет средство просмотра форм о том, что в форме загружено новое или существующее сообщение.
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно установлено.
    
## <a name="remarks"></a>Комментарии

Объекты формы вызывают метод **имапивиевадвисесинк:: онневмессаже** при каждом загрузке сообщения в форме с помощью метода [Иперсистмессаже:: инитнев](ipersistmessage-initnew.md) или [иперсистмессаже:: Load](ipersistmessage-load.md) . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Освободите активный указатель на объект формы, так как он больше не указывает на сообщение, которое ранее было проходило в вашем средстве просмотра. 
  
Дополнительные сведения об уведомлениях формы можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>См. также



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

