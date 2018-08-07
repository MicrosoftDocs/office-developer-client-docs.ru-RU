---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2eb92c3f1555407a77332bd6ec3b2b7202f0553f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812322"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Относится к**: Outlook 
  
Создает структуру [SSortOrderSet](ssortorderset.md) именованные, содержащий указанное число порядок сортировки. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Параметры

__csort_
  
> Число порядок сортировки должны быть включены в новой структуры.
    
_имя_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Используйте макрос **SizedSSortOrderSet** для создания набора с явные границы порядок сортировки. 
  
Для применения новой структуры, результаты из макроса **SizedSSortOrderSet** как указатель на структуру **SSortOrderSet** , выполните следующие приведения. 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>См. также

- [SSortOrderSet](ssortorderset.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

