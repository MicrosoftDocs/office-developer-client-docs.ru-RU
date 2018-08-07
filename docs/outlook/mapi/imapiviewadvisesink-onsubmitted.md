---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 40a72bed0b3e763ea482b228174b85d9f42185c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809236"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Относится к**: Outlook 
  
Уведомляет средство просмотра формы, что текущего сообщения были отправлены диспетчер очереди MAPI.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Уведомление успешно завершен.
    
## <a name="remarks"></a>Замечания

Объект формы вызывает метод **IMAPIViewAdviseSink::OnSubmitted** после успешного возврата вызова [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

После вызова **OnSubmitted** можно продолжить предполагается, что сообщение были обновлены. Обновление windows в соответствии с все изменения, произошедшие. 
  
Дополнительные сведения о уведомлений формы можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>См. также



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

