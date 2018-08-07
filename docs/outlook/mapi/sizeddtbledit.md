---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4ea77023bdc9442325f4af46d23c107e7172ceaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812297"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Относится к**: Outlook 
  
Создает именованный структуру, которая включает в себя структуры [DTBLEDIT](dtbledit.md) для описания элемента управления и максимальное число символов, которые могут быть введены в элементе управления. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Максимальное число символов, которые можно ввести в элемент управления для редактирования.
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **SizedDtblEdit** позволяет определить элемента управления, если известен число включенных символов. Новая структура создается с следующие элементы: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblEdit** как указатель на структуру **DTBLEDIT** , выполните следующие приведения: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>См. также

- [DTBLEDIT](dtbledit.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

