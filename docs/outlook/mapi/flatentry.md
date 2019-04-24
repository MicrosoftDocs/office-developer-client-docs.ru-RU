---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334820"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Структура [EntryID](entryid.md) и число байтов, определяющее размер структуры **EntryID** . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанные макросы:  <br/> |[кбфлатентри](cbflatentry.md), [кбневфлатентри](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>Members

 **cb**
  
> Количество байтов в элементе **абентри** . 
    
 **Абентри**
  
> Полный идентификатор записи, включающий массив флагов и двоичных данных.
    
## <a name="remarks"></a>Комментарии

Структура **флатентри** похожа на структуру [EntryID](entryid.md) . Однако существуют некоторые отличия. 
  
- В структуре **флатентри** хранится размер идентификатора записи; Идентификатор **EntryID** — нет. 
    
- Структура **флатентри** сохраняет данные флага вместе с остальной частью идентификатора записи; **EntryID** хранит их по отдельности. 
    
- Структура **флатентри** используется для хранения идентификатора записи в файле или его передачи в потоке байтов, в то время как структура **EntryID** используется методами интерфейса [IMAPIProp](imapipropiunknown.md) , а также следующими методами **OpenEntry** : [иаблогон: : OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md), [IMAPISession:: OpenEntry](imapisession-openentry.md), [Имаписуппорт:: OpenEntry](imapisupport-openentry.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md), [имслогон:: OpenEntry](imslogon-openentry.md)
    
- Структура **флатентри** используется для хранения идентификатора записи в файле или его передачи в потоке байтов. Структура **EntryID** используется для хранения идентификатора записи на диске. 
    
## <a name="see-also"></a>См. также



[КОД](entryid.md)


[Структуры MAPI](mapi-structures.md)

