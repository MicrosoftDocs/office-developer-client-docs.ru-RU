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
ms.openlocfilehash: 8d960207e05b33efe55886166ff1322f7f4eedce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586202"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает именованный структуру, которая включает в себя структуры [DTBLLABEL](dtbllabel.md) для описания элемента управления label и связанные метки заданной длины. 
  
|||
|:-----|:-----|
|Указанный в файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Длина метки. Этот компонент включает конечным символом NULL. 
    
_u_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **SizedDtblLabel** позволяет определить метки в таблице отображения при известные число символов в подписи. Новая структура создается с следующие элементы: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Чтобы использовать указатель в итоговый структуру из макроса **SizedDtblLabel** как указатель на структуру **DTBLLABEL** , выполните следующие приведения: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>См. также

- [DTBLLABEL](dtbllabel.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

