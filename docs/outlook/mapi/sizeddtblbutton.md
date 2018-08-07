---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812290"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**Относится к**: Outlook 
  
Создает именованный структуру, которая включает в себя структуры [DTBLBUTTON](dtblbutton.md) для описания кнопки и метки заданной длины. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>Параметры

 _n_
  
> Длина метки должны быть включены в новой структуры.
    
 _u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Новая структура создается с следующие элементы:
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>См. также



[DTBLBUTTON](dtblbutton.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

