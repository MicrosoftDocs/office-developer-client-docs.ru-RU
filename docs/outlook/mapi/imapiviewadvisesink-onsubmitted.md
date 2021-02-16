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
ms.openlocfilehash: ebde06d0d22320ecb5edb633cf8d04aaeec2a841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433985"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сообщает просмотру формы, что текущее сообщение отправлено в пул MAPI.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно.
    
## <a name="remarks"></a>Примечания

Объект формы вызывает метод **IMAPIViewAdviseSink::OnSubmitted** после успешного возврата вызова [IMAPIMessageSite::SubmitMessage.](imapimessagesite-submitmessage.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

После того как будет вызвана **onSubmitted,** можно продолжить, предполагая, что сообщение было обновлено. Обновите окна, чтобы отразить все внесенные изменения. 
  
Дополнительные сведения об уведомлениях о формах см. в сведениях об отправке и [получении уведомлений о формах.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>См. также



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

