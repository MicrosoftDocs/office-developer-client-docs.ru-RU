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
ms.openlocfilehash: ae3f84c6b219c7becb88737f0d6c9fcb9722ea34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584970"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создание именованного структуру, которая включает в себя структуры [DTBLPAGE](dtblpage.md) для описания элемента управления вкладки, метки заданной длины и запись в файле справки заданной длины. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Длина метки для вкладку страница.
    
_N1_
  
> Длина записи, изображения которых появляются в файла Mapisvc.inf, идентифицирующий файл справки, который будет использоваться с элементом управления страницы с вкладками.
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **SizedDtblPage** позволяет определить элемент управления вкладки при известно количество символов в связанные метки и запись файла справки. Новая структура создается с следующие элементы: 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblPage** как указатель на структуру **DTBLPAGE** , выполните следующие приведения: 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>См. также

- [DTBLPAGE](dtblpage.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

