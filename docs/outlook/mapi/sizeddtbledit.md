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
  
Создает именованную структуру, включающую структуру [дтбледит](dtbledit.md) для описания элемента управления Editing и максимальное количество символов, которое можно ввести в элемент управления. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Максимальное количество символов, которое можно ввести в поле редактирования.
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Примечания

Макрос **сизеддтбледит** позволяет определить элемент управления редактированием, если известно количество включенных символов. Новая структура создается со следующими элементами: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Чтобы использовать указатель на полученную структуру из макроса **сизеддтбледит** в качестве указателя структуры **дтбледит** , выполните следующую операцию приведения: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>См. также

- [DTBLEDIT](dtbledit.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

