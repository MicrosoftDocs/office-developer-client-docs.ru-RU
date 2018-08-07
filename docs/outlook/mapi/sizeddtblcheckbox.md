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
ms.openlocfilehash: 9a30554253bc11c8905273079429e4b41c20583a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812292"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**Относится к**: Outlook 
  
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

