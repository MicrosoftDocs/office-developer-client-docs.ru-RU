---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fea2b496a34d7aa7f9469158fae14daf6a770608
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812309"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**Относится к**: Outlook 
  
Создает именованные структуру, которая включает в себя структуры [DTBLCOMBOBOX](dtblcombobox.md) для описания поле со списком и максимальное число символов, которые можно ввести в окне связанный редактирования. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Число знаков, которое можно ввести в поле со списком редактирование элемента управления. 
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **SizedDtblComboBox** позволяет определить поле со списком при известные длина строки включено символов. Новая структура создается с следующие элементы: 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblComboBox** как указатель на структуру **DTBLCOMBOBOX** , выполните следующие приведения: 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>См. также

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)
