---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576206"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет формы для изменения, внесенные с момента последнего сохранения.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Параметры

None
  
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Форма содержит изменения, внесенные с момента последнего сохранения.
    
S_FALSE 
  
> Форма не имеет изменения, внесенные с момента последнего сохранения.
    
## <a name="remarks"></a>Замечания

Средства просмотра формы вызовите метод **IPersistMessage::IsDirty** , чтобы определить, имеет ли сообщение несохраненные данные. 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

