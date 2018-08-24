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
ms.openlocfilehash: 054625601b496a8ec8f7745aa4cbc4715eed81a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585061"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описание ограничений **или** , в которой используется для применения логической операции **или** ограничение. 
  
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

## <a name="members"></a>Members

 **cRes**
  
> Число структур в массиве, на который указывает член **lpRes** . 
    
 **lpRes**
  
> Указатель на структуру [SRestriction](srestriction.md) , описывающий ограничения для объединения с помощью логической операции **или** . 
    
## <a name="remarks"></a>Замечания

Дополнительные сведения о структуре **SOrRestriction** [О ограничения](about-restrictions.md)см. 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

