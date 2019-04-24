---
title: Иперсистмессажеисдирти
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309613"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет форму на наличие изменений, выполненных с момента последнего сохранения.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма содержит изменения, внесенные с момента последнего сохранения.
    
S_FALSE 
  
> В форме не внесены изменения, внесенные с момента последнего сохранения.
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызывают метод **иперсистмессаже:: IsDirty** , чтобы определить, содержит ли сообщение несохраненные данные. 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

