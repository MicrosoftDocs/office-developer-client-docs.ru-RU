---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 943dab0141581adc32c184b0042a063a4ec05c3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582884"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет тег указанного свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Параметры

 _ulPropTag_
  
> [in] Свойство tag для проверки.
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Тег указанное свойство не является допустимым тегом свойство MAPI. 
    
FALSE 
  
> Тег указанное свойство является допустимым тегом свойство MAPI.
    
## <a name="remarks"></a>Замечания

Функция **FBadPropTag** проверяет указанное свойство tag, на основе MAPI определений. Он сделать sures, тип свойства — это один из типов, определенных параметром MAPI, который идентификатор свойства определяется как этого типа. 
  
## <a name="see-also"></a>См. также



[FBadProp](fbadprop.md)

