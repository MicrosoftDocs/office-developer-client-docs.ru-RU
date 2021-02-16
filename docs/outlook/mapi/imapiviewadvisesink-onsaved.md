---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407608"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сообщает просмотру формы о том, что текущее сообщение в форме сохранено.
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Объект формы вызывает метод **IMAPIViewAdviseSink::OnSaved** после успешного с сохранения текущего сообщения в форме. Это позволяет зрителям обновлять окна, чтобы отразить изменения в сообщении. 
  
Дополнительные сведения об уведомлениях форм см. в подкассылной форме отправки [и получения уведомлений.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>См. также



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

