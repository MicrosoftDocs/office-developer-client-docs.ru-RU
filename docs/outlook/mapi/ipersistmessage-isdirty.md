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
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407573"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет форму для изменений, которые были сделаны с момента последнего сохранения.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма имеет изменения, которые были сделаны с момента ее последнего сэкономленного.
    
S_FALSE 
  
> Форма не имеет изменений, которые были внесены с момента ее последнего сэкономленного.
    
## <a name="remarks"></a>Примечания

Зрители формы звонят **по методу IPersistMessage::IsDirty,** чтобы определить, есть ли в сообщении неопределяемые данные. 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

