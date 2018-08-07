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
ms.openlocfilehash: 2f5f4d50b085c437d1caab5f70dcb741afe090bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808446"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**Относится к**: Outlook 
  
Кроме того в байтах, задающее размер структуры **ENTRYID** структуру [ENTRYID](entryid.md) . 
  
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

## <a name="members"></a>Members

 **cb**
  
> Число байт в элемент **abEntry** . 
    
 **abEntry**
  
> Идентификатор полная запись, которая включает в себя массив флаги и двоичных данных.
    
## <a name="remarks"></a>Замечания

Структура **FLATENTRY** напоминает структуру [ENTRYID](entryid.md) . Тем не менее существуют некоторые отличия: 
  
- Структура **FLATENTRY** сохраняет размер идентификатор записи; **Идентификатор записи** — нет. 
    
- Структура **FLATENTRY** хранит данные флаг с другими идентификатор записи; **Идентификатор записи** сохраняет их отдельно. 
    
- Структура **FLATENTRY** используется для хранения идентификатора записи в файле и передайте его в поток байтов, то время как структуру **ENTRYID** используется путем методов интерфейса [IMAPIProp](imapipropiunknown.md) и следующие методы **OpenEntry** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Структура **FLATENTRY** используется для хранения идентификатора записи в файл или передайте его в виде потока в байтах. Структура **ENTRYID** используется для хранения идентификатора записи на диск. 
    
## <a name="see-also"></a>См. также



[ENTRYID](entryid.md)


[Структуры MAPI](mapi-structures.md)

