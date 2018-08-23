---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 00c7560427ece58026030ce6895d60aec7cc5a2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570943"
---
# <a name="iid"></a>IID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описывает структуру [идентификатор GUID](guid.md) , используемый для описания идентификатор для интерфейса MAPI. 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

Просмотр структуры **GUID** . 
  
## <a name="remarks"></a>Замечания

**ИД интерфейса** структура используется для уникальной идентификации интерфейса MAPI и связывание определенного интерфейса с помощью объекта. Например при вызовах клиента [IMAPISession::OpenEntry](imapisession-openentry.md) чтобы открыть папку, клиент задается параметр _lpInterface_ для указания на **ИД интерфейса** представляющее интерфейс [IMAPIFolder](imapifolderimapicontainer.md) . MAPI определяет **IMAPIFolderIID** быть IID_IMAPIFolder. **ИД интерфейса** структуры также используются для уникальной идентификации интерфейсов OLE. 
  
Все определенные структуры **ИД интерфейса** MAPI интерфейсов определены в файле заголовка Mapiguid.h. 
  
## <a name="see-also"></a>См. также



[ИДЕНТИФИКАТОР GUID](guid.md)


[Структуры MAPI](mapi-structures.md)

