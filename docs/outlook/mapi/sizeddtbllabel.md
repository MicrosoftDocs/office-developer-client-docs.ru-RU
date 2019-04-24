---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282707"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру, которая включает структуру [дтбллабел](dtbllabel.md) для описания элемента управления Label и связанную метку заданной длины. 
  
|||
|:-----|:-----|
|Указано в файле заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Длина метки. Сюда входит конечный символ NULL. 
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **сизеддтбллабел** позволяет определить метку отображаемой таблицы, когда число символов в метке известно. Новая структура создается со следующими элементами: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Чтобы использовать указатель на полученную структуру из макроса **сизеддтбллабел** в качестве указателя структуры **дтбллабел** , выполните следующую операцию приведения: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>См. также

- [DTBLLABEL](dtbllabel.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

