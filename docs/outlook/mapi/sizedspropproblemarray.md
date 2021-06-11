---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418115"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает структуру [SPropProblemArray](spropproblemarray.md) с заданным числом [структур SPropProblem.](spropproblem.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parameters

_ _cprob_
  
> Количество **структур SPropProblem,** которые будут включены в новую структуру. 
    
_ _имя_
  
> Имя новой структуры.
    
## <a name="remarks"></a>Примечания

Используйте **макрос SizedSPropProblemArray** для создания массива проблем свойств с явными границами. Чтобы использовать новую структуру, которая является результатом макроса **SizedSPropProblemArray** в качестве указателя на структуру **SPropProblemArray,** выполните следующий бросок: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>См. также

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

