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
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416267"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру, включающую структуру [дтблкомбобокс](dtblcombobox.md) для описания элемента управления "поле со списком" и максимальное количество символов, которое можно ввести в связанный элемент управления редактирования. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Число символов, которое можно ввести в поле ввода поля со списком. 
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Примечания

С помощью макроса **сизеддтблкомбобокс** можно определить поле со списком, если известна длина строки разрешенных символов. Новая структура создается со следующими элементами: 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Чтобы использовать указатель на полученную структуру из макроса **сизеддтблкомбобокс** в качестве указателя структуры **дтблкомбобокс** , выполните следующую операцию приведения: 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>См. также

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

