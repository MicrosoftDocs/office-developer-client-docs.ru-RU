---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428608"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает именоваемую [структуру SSortOrderSet,](ssortorderset.md) которая содержит указанное число заказов на сортировку. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Параметры

_ _csort_
  
> Количество заказов сортировки, которые необходимо включить в новую структуру.
    
_ _name_
  
> Имя новой структуры.
    
## <a name="remarks"></a>Примечания

Используйте **макрос SizedSSortOrderSet,** чтобы создать порядок сортировки с явными границами. 
  
Чтобы использовать новую структуру, которая является результатом выполнения **макроса SizedSSortOrderSet** в качестве указателя на структуру **SSortOrderSet,** выполните следующую пристановка: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>См. также

- [SSortOrderSet](ssortorderset.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

