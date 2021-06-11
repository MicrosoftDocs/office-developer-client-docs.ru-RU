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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420810"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру, которая включает структуру [DTBLCHECKBOX](dtblcheckbox.md) для описания управления контрольным окном и метки определенной длины. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>Parameters

_n_
  
> Длина метки, которая будет включена в новую структуру.
    
_u_
  
> Имя новой структуры.
    
## <a name="remarks"></a>Примечания

Макрос **SizedDtblCheckBox** позволяет определить контрольный ящик, если известно число символов метки. Новая структура создается со следующими участниками: 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Чтобы использовать указатель на следующую структуру из **макроса SizedDtblCheckBox** в качестве указателя **структуры DTBLCHECKBOX,** выполните следующий бросок: 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>См. также

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

