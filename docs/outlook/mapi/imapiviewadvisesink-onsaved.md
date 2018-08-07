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
ms.openlocfilehash: 0f9aa5d508afeaf5933c50763e1e42832ae4e3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809249"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**Относится к**: Outlook 
  
Уведомляет средство просмотра формы, который был сохранен текущего сообщения в форме.
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Объект формы вызывает метод **IMAPIViewAdviseSink::OnSaved** после сохранения текущего сообщения в форме. Это позволяет использовать средства просмотра для обновления их windows сведения об изменениях в сообщение. 
  
Дополнительные сведения о уведомлений формы можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>См. также



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

