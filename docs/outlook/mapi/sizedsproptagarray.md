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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429350"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает именоваемую [структуру SPropTagArray,](sproptagarray.md) которая включает указанное число тегов свойств. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Параметры

_ _ctag_
  
> Количество тегов свойств, которые необходимо включить в новую структуру.
    
_ _name_
  
> Имя новой структуры.
    
## <a name="remarks"></a>Примечания

Используйте **макрос SizedSPropTagArray** для создания массива тегов свойств с явными границами. 
  
Чтобы использовать новую структуру, которая является результатом макроса **SizedSPropTagArray** в качестве указателя на структуру **SPropTagArray,** выполните следующую пристановку: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>См. также

- [SPropTagArray](sproptagarray.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

