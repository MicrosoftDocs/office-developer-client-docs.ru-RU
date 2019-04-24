---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282756"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру, которая включает структуру [дтблчеккбокс](dtblcheckbox.md) для описания элемента управления "флажок" и метку указанной длины. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Длина метки, которая должна быть включена в новую структуру.
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **сизеддтблчеккбокс** позволяет установить флажок, если число символов в метке известно. Новая структура создается со следующими элементами: 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Чтобы использовать указатель на полученную структуру из макроса **сизеддтблчеккбокс** в качестве указателя структуры **дтблчеккбокс** , выполните следующую операцию приведения: 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>См. также

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

