---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410933"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру [SRowSet](srowset.md) , которая содержит указанное количество строк. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Параметры

__CRowset_
  
> Количество строк, включаемых в новую структуру.
    
__имя_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Примечания

Чтобы использовать новую структуру, полученную из макроса **сизедсровсет** в качестве указателя на структуру **SRowSet** , выполните приведенные ниже действия. 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>См. также

- [SRowSet](srowset.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

