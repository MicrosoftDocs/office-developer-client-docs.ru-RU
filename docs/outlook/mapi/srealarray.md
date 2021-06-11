---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429875"
---
# <a name="srealarray"></a>SRealArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив значений float, используемых для описания свойства типа PT_MV_R4. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество значений в массиве, на который указывает член **lpflt.** 
    
 **lpflt**
  
> Указатель на массив значений float.
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о типе PT_MV_R4 см. введите [Типы свойств.](property-types.md)
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

