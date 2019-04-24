---
title: Имапивиевадвисесинконсубмиттед
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351172"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Уведомляет средство просмотра форм о том, что текущее сообщение было отправлено в Диспетчер очереди MAPI.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно установлено.
    
## <a name="remarks"></a>Примечания

Объект Form вызывает метод **имапивиевадвисесинк::** onsubmittedся после вызова [Имапимессажесите:: субмитмессаже](imapimessagesite-submitmessage.md) успешно возвращен. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

После **** вызова OnSubmitted можно продолжить предположение о том, что сообщение было обновлено. Обновите Windows, чтобы отразить все произошедшие изменения. 
  
Дополнительные сведения об уведомлениях формы можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>См. также



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

