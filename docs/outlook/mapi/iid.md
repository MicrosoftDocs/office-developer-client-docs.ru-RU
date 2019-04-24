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
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336353"
---
# <a name="iid"></a>IID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает структуру [GUID](guid.md) , используемую для описания идентификатора интерфейса MAPI. 
  
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
  
## <a name="remarks"></a>Комментарии

Структура **IID** используется для уникальной идентификации интерфейса MAPI и связывания определенного интерфейса с объектом. Например, когда клиент вызывает [IMAPISession:: OpenEntry](imapisession-openentry.md) , чтобы открыть папку, клиент устанавливает параметр _лпинтерфаце_ , который указывает на **IID** , представляющий интерфейс [IMAPIFolder](imapifolderimapicontainer.md) . MAPI определяет **имапифолдериид** для иид_имапифолдер. Структуры **IID** также используются для уникальной идентификации интерфейсов OLE. 
  
Все конкретные структуры **IID** для интерфейсов MAPI определены в файле заголовка мапигуид. h. 
  
## <a name="see-also"></a>См. также



[GUID](guid.md)


[Структуры MAPI](mapi-structures.md)

