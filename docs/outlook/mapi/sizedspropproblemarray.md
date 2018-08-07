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
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812304"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Относится к**: Outlook 
  
Создает структуру [SPropProblemArray](spropproblemarray.md) именованные, содержащий указанное число [SPropProblem](spropproblem.md) структуры. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Параметры

__cprob_
  
> Число структур **SPropProblem** должны быть включены в новой структуры. 
    
_имя_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Используйте макрос **SizedSPropProblemArray** для создания массива проблема свойства с помощью явных границы. Для применения новой структуры, результаты из макроса **SizedSPropProblemArray** как указатель на структуру **SPropProblemArray** , выполните следующие приведения. 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>См. также

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

