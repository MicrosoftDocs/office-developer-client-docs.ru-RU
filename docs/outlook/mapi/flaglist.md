---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412977"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит список флагов, используемых для указать состояние записей адресов во время процесса разрешения имен.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>"Участники"

 **cFlags**
  
> Количество флагов, определенных MAPI в списке.
    
 **ulFlags**
  
> Массив флагов, которые обеспечивают состояние операции разрешения имен для получателя. Можно установить следующие флаги:
    
MAPI_AMBIGUOUS 
  
> Получатель был решен, но не для уникального идентификатора записи. Другие контейнеры адресной книги не должны пытаться устранить этого получателя. 
    
MAPI_RESOLVED 
  
> Получатель был решен с уникальным идентификатором записи. Другие контейнеры адресной книги не должны пытаться устранить этого получателя. 
    
MAPI_UNRESOLVED 
  
> Запись не разрешена. Другие контейнеры адресной книги должны попытаться устранить этого получателя.
    
## <a name="remarks"></a>Примечания

Структура **FLAGLIST** используется в качестве параметра [для IABContainer::ResolveNames.](iabcontainer-resolvenames.md) Каждый из получателей, которые будут решены, входит в структуру [ADRLIST.](adrlist.md) Когда контейнер адресной книги пытается разрешить каждого получателя, он задает соответствующий флаг в соответствующей записи в **структуре FLAGLIST.** Все записи в структуре **FLAGLIST** находятся в том же порядке, что и записи в **структуре ADRLIST.** Это упрощает связывать параметр флага с получателем. 
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Структуры MAPI](mapi-structures.md)

