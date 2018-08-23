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
ms.openlocfilehash: be41a9916b6b231d5715cf18fe2b0d804434f2ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594483"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Определяет данные закладки запоминание позицию в таблице. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные методы:  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Замечания

MAPI определяет три закладки, перечисленных следующим образом:
  
BOOKMARK_BEGINNING 
  
> Запоминает позицию в таблице. 
    
BOOKMARK_CURRENT 
  
> Запоминает сведения о текущей позиции в таблице.
    
BOOKMARK_END 
  
> Запоминает конечную позицию в таблице.
    
Клиенты могут создавать другие закладки запоминание другие положения в таблице. Закладки являются допустимыми только когда таблица открыта. Клиенты необходимо освободить все закладки, которые они созданы перед закрытием в связанной таблице. 
  
## <a name="see-also"></a>См. также



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Типы данных MAPI](mapi-data-types.md)

