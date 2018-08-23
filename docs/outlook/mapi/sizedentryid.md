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
ms.openlocfilehash: d797acdbf2abfb88151d69d0c93e743f07afc5c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563872"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает структуру [ENTRYID](entryid.md) именованные, содержащего члены **ab** указанного размера. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Параметры

__Сертификация_
  
> Число байт в член **ab** новой структуры. 
    
_имя_
  
> Имя для новой структуры.
    
## <a name="remarks"></a>Замечания

Макрос **SizedENTRYID** позволяет определить идентификатор записи после известные требования к длине массива. Используйте этот макрос для создания идентификатора запись с явные границы. 
  
Для применения новой структуры, результаты из макроса **SizedENTRYID** как указатель на структуру **ENTRYID** , выполните следующие приведения. 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>См. также

- [ENTRYID](entryid.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

