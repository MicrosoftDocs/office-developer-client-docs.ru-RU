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
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282700"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру [спроптагаррай](sproptagarray.md) , которая включает указанное количество тегов свойств. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Параметры

__ctag_
  
> Количество тегов свойств, включаемых в новую структуру.
    
__имя_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

С помощью макроса **сизедспроптагаррай** создайте массив тегов свойств с явными границами. 
  
Чтобы использовать новую структуру, полученную из макроса **сизедспроптагаррай** в качестве указателя на структуру **спроптагаррай** , выполните приведенные ниже действия. 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>См. также

- [SPropTagArray](sproptagarray.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

