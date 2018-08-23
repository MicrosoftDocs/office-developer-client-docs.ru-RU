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
ms.openlocfilehash: 7e50589b52f3e99bf2569a55bb7d3ca4f8247fd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591662"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

