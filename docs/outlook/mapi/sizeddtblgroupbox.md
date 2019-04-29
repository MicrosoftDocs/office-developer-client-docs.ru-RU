---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419319"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру, которая включает структуру [дтблграупбокс](dtblgroupbox.md) для описания элемента управления "Группа" и метку указанной длины. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Длина метки поля группы. 
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Примечания

Макрос **сизеддтблграупбокс** позволяет определить элемент управления поля группы, если длина метки известна. Новая структура создается со следующими элементами: 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Чтобы использовать указатель на полученную структуру из макроса **сизеддтблграупбокс** в качестве указателя структуры **дтблграупбокс** , выполните следующую операцию приведения: 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>См. также

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

