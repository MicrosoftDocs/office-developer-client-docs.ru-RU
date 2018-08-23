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
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572566"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

