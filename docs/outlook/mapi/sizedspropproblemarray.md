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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282693"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру [спроппроблемаррай](spropproblemarray.md) , содержащую указанное число структур [спроппроблем](spropproblem.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Параметры

__кпроб_
  
> Количество структур **спроппроблем** , включаемых в новую структуру. 
    
__имя_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

С помощью макроса **сизедспроппроблемаррай** создайте массив проблем свойств с явными границами. Чтобы использовать новую структуру, полученную из макроса **сизедспроппроблемаррай** в качестве указателя на структуру **спроппроблемаррай** , выполните приведенные ниже действия. 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>См. также

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

