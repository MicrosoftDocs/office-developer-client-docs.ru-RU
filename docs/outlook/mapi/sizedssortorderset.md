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
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428608"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру [ссортордерсет](ssortorderset.md) , содержащую указанное число порядков сортировки. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Параметры

__ксорт_
  
> Количество порядков сортировки, включаемых в новую структуру.
    
__имя_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Примечания

Используйте макрос **сизедссортордерсет** для создания набора порядка сортировки с явными границами. 
  
Чтобы использовать новую структуру, полученную из макроса **сизедссортордерсет** в качестве указателя на структуру **ссортордерсет** , выполните приведенные ниже действия. 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>См. также

- [SSortOrderSet](ssortorderset.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

