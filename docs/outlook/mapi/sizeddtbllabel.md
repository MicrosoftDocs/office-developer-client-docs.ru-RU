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
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812314"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Относится к**: Outlook 
  
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

