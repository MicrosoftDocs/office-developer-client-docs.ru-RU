---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437933"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение **OR,** которое используется для применения логической **операции or** к ограничению. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a>"Участники"

 **cRes**
  
> Количество структур в массиве, на который указывает член **lpRes.** 
    
 **lpRes**
  
> Указатель на [структуру SRestriction,](srestriction.md) описывающий ограничение, к нему необходимо присоединяться с помощью логической **операции OR.** 
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о структуре **SOrRestriction** см. в дополнительных [сведениях об ограничениях.](about-restrictions.md) 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

