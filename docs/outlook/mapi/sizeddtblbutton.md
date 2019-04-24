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
ms.openlocfilehash: a7d62d29638ae234667eb33a8103fb3a716afc32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282763"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру, включающую структуру [дтблбуттон](dtblbutton.md) для описания кнопки и метки заданной длины. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>Параметры

 _n_
  
> Длина метки, которая должна быть включена в новую структуру.
    
 _u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Новая структура создается со следующими элементами:
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>См. также



[DTBLBUTTON](dtblbutton.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

