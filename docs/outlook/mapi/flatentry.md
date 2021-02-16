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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407244"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Структура [ENTRYID](entryid.md) и количество byte, которое определяет размер **структуры ENTRYID.** 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>"Участники"

 **cb**
  
> Количествобайтов в **члене abEntry.** 
    
 **abEntry**
  
> Полный идентификатор записи, который включает массив флагов и двоичных данных.
    
## <a name="remarks"></a>Примечания

Структура **FLATENTRY** похожа на [структуру ENTRYID.](entryid.md) Однако существуют некоторые различия: 
  
- В **структуре FLATENTRY** хранится размер идентификатора записи; **ENTRYID** этого не делает. 
    
- Структура **FLATENTRY** сохраняет данные флага вместе с остальным идентификатором записи; **ENTRYID** хранит их отдельно. 
    
- Структура **FLATENTRY** используется для хранения идентификатора записи в файле или передачи его в потоке в битах, тогда как структура **ENTRYID** используется методами интерфейса [IMAPIProp](imapipropiunknown.md) и следующими методами **OpenEntry:** [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Структура **FLATENTRY** используется для хранения идентификатора записи в файле или передачи его в потоке данных. Структура **ENTRYID** используется для хранения идентификатора записи на диске. 
    
## <a name="see-also"></a>См. также



[ENTRYID](entryid.md)


[Структуры MAPI](mapi-structures.md)

