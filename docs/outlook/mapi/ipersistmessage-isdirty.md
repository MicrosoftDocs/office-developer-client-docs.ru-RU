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
ms.openlocfilehash: e748427b39418a80cae88e98b4aa7eef6df24393
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809497"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Относится к**: Outlook 
  
Проверяет формы для изменения, внесенные с момента последнего сохранения.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Форма содержит изменения, внесенные с момента последнего сохранения.
    
S_FALSE 
  
> Форма не имеет изменения, внесенные с момента последнего сохранения.
    
## <a name="remarks"></a>Замечания

Средства просмотра формы вызовите метод **IPersistMessage::IsDirty** , чтобы определить, имеет ли сообщение несохраненные данные. 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

