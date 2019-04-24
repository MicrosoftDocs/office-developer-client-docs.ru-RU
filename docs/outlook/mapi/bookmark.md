---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318041"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет данные закладок для запоминания положения в таблице. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанные методы:  <br/> |[IMAPITable:: креатебукмарк](imapitable-createbookmark.md) [IMAPITable:: фрибукмарк](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Замечания

MAPI определяет три закладки, перечисленные ниже.
  
БУКМАРК_БЕГИННИНГ 
  
> Запоминает начальную позицию таблицы. 
    
БУКМАРК_КУРРЕНТ 
  
> Запоминает текущую позицию таблицы.
    
БУКМАРК_ЕНД 
  
> Запоминает конечное положение таблицы.
    
Клиенты могут создавать другие закладки для запоминания других положений таблиц. Закладки действительны только в том случае, если таблица открыта. Перед закрытием связанной таблицы Клиенты должны освободить все созданные вами закладки. 
  
## <a name="see-also"></a>См. также



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Типы данных MAPI](mapi-data-types.md)

