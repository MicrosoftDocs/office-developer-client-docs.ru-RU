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
ms.openlocfilehash: a0e859ac0f8bcc3bd83e336c85da21f1251efcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808811"
---
# <a name="iid"></a>IID

  
  
**Относится к**: Outlook 
  
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



[GUID](guid.md)


[Структуры MAPI](mapi-structures.md)

