---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431122"
---
# <a name="currency"></a>CURRENCY

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит подписанное 64-битное значение, представляющее значение валюты. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a>"Участники"

 **Lo**
  
> 32 бита валюты низкого порядка. 
    
 **Привет**
  
> 32 бита валюты в высоком порядке.
    
## <a name="remarks"></a>Примечания

Структура **CURRENCY** — это масштабное integer-представление десятичной цифры с четырьмя цифрами справа от десятичной точки. Например, сохраненное значение 327500 следует представить как значение валюты 32,7500. 
  
Структура **CURRENCY** используется для описания свойства типа PT_CURRENCY. Сведения о типах свойств см. в обзоре [типов свойств MAPI.](mapi-property-type-overview.md)
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

