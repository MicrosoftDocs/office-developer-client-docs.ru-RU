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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405711"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает именоваемую [структуру ENTRYID,](entryid.md) которая содержит **аб-член** указанного размера. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Parameters

_ _cb_
  
> Количество bytes в **аб-члене** новой структуры. 
    
_ _имя_
  
> Имя новой структуры.
    
## <a name="remarks"></a>Примечания

Макрос **SizedENTRYID** позволяет определить идентификатор записи после того, как будут известны требования к длине массива. Используйте этот макрос для создания идентификатора записи с явными границами. 
  
Чтобы использовать новую структуру, которая является результатом макроса **SizedENTRYID** в качестве указателя на **структуру ENTRYID,** выполните следующие броски: 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>См. также

- [ENTRYID](entryid.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

