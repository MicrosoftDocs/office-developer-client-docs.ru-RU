---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282659"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру, которая включает структуру [дтблпаже](dtblpage.md) для описания элемента управления страницы с вкладками, метку указанной длины и запись файла справки с указанной длиной. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Длина метки для вкладки страницы.
    
_N1_
  
> Длина записи в файле Mapisvc. INF, определяющая файл справки, который будет использоваться с элементом управления со вкладками.
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **сизеддтблпаже** позволяет определить элемент управления со вкладками, если известно число символов в связанной метке и записи файла справки. Новая структура создается со следующими элементами: 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Чтобы использовать указатель на полученную структуру из макроса **сизеддтблпаже** в качестве указателя структуры **дтблпаже** , выполните следующую операцию приведения: 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>См. также

- [DTBLPAGE](dtblpage.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

