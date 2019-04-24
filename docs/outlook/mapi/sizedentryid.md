---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282686"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает именованную структуру [EntryID](entryid.md) , содержащую элемент **AB** указанного размера. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**КОД** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Параметры

__CB_
  
> Количество байтов в элементе **AB** новой структуры. 
    
__имя_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **сизедентрид** позволяет определить идентификатор записи после того, как будут известны требования к длине массива. Используйте этот макрос для создания идентификатора записи с явно заданными границами. 
  
Чтобы использовать новую структуру, полученную из макроса **сизедентрид** в качестве указателя на структуру **EntryID** , выполните приведенные ниже действия. 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>См. также

- [КОД](entryid.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

