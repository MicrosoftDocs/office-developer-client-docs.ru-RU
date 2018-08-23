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
ms.openlocfilehash: dc4d3a7a827e728dfd6725ac269350067d4530cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590346"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

