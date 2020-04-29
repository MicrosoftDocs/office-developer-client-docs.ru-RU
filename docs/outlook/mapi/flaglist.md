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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список флагов, используемых для указания состояния записей адресов в процессе разрешения имен.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>"Участники"

 **кфлагс**
  
> Количество флагов, определенных MAPI, в списке.
    
 **ulFlags**
  
> Массив флагов, который предоставляет состояние операции разрешения имен для получателя. Можно задать следующие флаги:
    
MAPI_AMBIGUOUS 
  
> Получатель разрешен, но не является уникальным идентификатором записи. Другие контейнеры адресных книг не должны пытаться разрешить этого получателя. 
    
MAPI_RESOLVED 
  
> Получатель был сопоставлен с уникальным идентификатором записи. Другие контейнеры адресных книг не должны пытаться разрешить этого получателя. 
    
MAPI_UNRESOLVED 
  
> Запись не была устранена. Другие контейнеры адресных книг должны попытаться разрешить этого получателя.
    
## <a name="remarks"></a>Примечания

Структура **флаглист** используется в качестве параметра для [Иабконтаинер:: ResolveNames](iabcontainer-resolvenames.md). Каждый из разрешенных получателей включается в структуру [ADRLIST](adrlist.md) . Так как контейнер адресной книги пытается разрешить каждого получателя, он устанавливает соответствующий флаг в соответствующей записи структуры **флаглист** . Все записи в структуре **флаглист** находятся в том же порядке, что и записи в структуре **ADRLIST** . Это позволяет легко сопоставить параметр флага с получателем. 
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Структуры MAPI](mapi-structures.md)

