---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7505c5dbcfc98a8b868424ae51cbe9c47b1d4338
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812307"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Относится к**: Outlook 
  
Создает структуру [SPropTagArray](sproptagarray.md) именованные, содержащий указанное число тегов свойств. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Параметры

__ctag_
  
> Число теги свойства должны быть включены в новой структуры.
    
_имя_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Используйте макрос **SizedSPropTagArray** для создания массива тега свойства с помощью явных границы. 
  
Для применения новой структуры, результаты из макроса **SizedSPropTagArray** как указатель на структуру **SPropTagArray** , выполните следующие приведения. 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>См. также

- [SPropTagArray](sproptagarray.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

