---
title: иперсистмессажеисдирти
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>Примечания

Средства просмотра форм вызывают метод **иперсистмессаже:: IsDirty** , чтобы определить, содержит ли сообщение несохраненные данные. 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

