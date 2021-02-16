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
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437646"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру, включаемую в себя структуру [DTBLEDIT](dtbledit.md) для описания управления редактированием и максимального количества символов, которые могут быть введены в этот список. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Максимальное количество символов, которые могут быть введены в управление редактированием.
    
_u_
  
> Имя новой структуры.
    
## <a name="remarks"></a>Примечания

Макрос **SizedDtblEdit** позволяет определить управление редактированием, если известно количество включенных символов. Новая структура создается с помощью следующих членов: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Чтобы использовать указатель на итоговую структуру из **макроса SizedDtblEdit** в качестве указателя структуры **DTBLEDIT,** выполните следующую привязку: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>См. также

- [DTBLEDIT](dtbledit.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

