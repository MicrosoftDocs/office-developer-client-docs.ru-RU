---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413607"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив строк символов, используемых для описания свойства типа PT_MV_UNICODE. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество строк в массиве, на который указывает **член lppszW.** 
    
 **lppszW**
  
> Указатель на массив null-ended строки символов Юникод.
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о PT_MV_UNICODE см. в [дополнительных сведениях о типах свойств.](property-types.md)
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

