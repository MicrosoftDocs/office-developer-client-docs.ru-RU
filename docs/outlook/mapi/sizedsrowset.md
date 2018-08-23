---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b8c70c8b13025f196fdebb2956939bec840a96f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583941"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает структуру [SRowSet](srowset.md) именованные, содержащий указанное число строк. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Параметры

__crow_
  
> Количество строк должны быть включены в новой структуры.
    
_имя_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Для применения новой структуры, результаты из макроса **SizedSRowSet** как указатель на структуру **SRowSet** , выполните следующие приведения. 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>См. также

- [SRowSet](srowset.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

