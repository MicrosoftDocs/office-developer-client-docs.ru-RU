---
title: Закладка
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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 8f5f3bc454e18b1dbab434fc1b7cc094b0d6a360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808283"
---
# <a name="bookmark"></a>Закладка

  
  
**Применимо к**: Outlook 
  
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


[���� ������ MAPI](mapi-data-types.md)

