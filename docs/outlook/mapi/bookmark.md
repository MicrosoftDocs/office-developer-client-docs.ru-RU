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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418136"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет данные закладок для запоминания позиции в таблице. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные методы:  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Примечания

MAPI определяет три закладки, перечисленные ниже.
  
BOOKMARK_BEGINNING 
  
> Запоминает начальное положение таблицы. 
    
BOOKMARK_CURRENT 
  
> Запоминает текущее положение таблицы.
    
BOOKMARK_END 
  
> Запоминает конечную позицию таблицы.
    
Клиенты могут создавать другие закладки для запоминания других позиций таблиц. Закладки действительны только в том случае, если таблица открыта. Клиенты должны освободить все созданные им закладки перед закрытием связанной таблицы. 
  
## <a name="see-also"></a>См. также



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Типы данных MAPI](mapi-data-types.md)

