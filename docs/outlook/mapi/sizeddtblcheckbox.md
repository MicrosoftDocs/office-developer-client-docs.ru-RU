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
ms.openlocfilehash: 6120439ea0d98ed6b64fe1542a4372265574723a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567533"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает именованный структуру, которая включает в себя структуры [DTBLCHECKBOX](dtblcheckbox.md) для описания элемента управления "флажок" и метки заданной длины. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Длина метки должны быть включены в новой структуры.
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **SizedDtblCheckBox** позволяет определить флажок при известные число знаков метки. Новая структура создается с следующие элементы: 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblCheckBox** как указатель на структуру **DTBLCHECKBOX** , выполните следующие приведения: 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>См. также

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

