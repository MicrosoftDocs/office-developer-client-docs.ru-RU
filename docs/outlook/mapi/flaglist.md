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
ms.openlocfilehash: 2cf5ff69e8453b2da26fd5044823ddf4f99a9f45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808451"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**Относится к**: Outlook 
  
Содержит список флагов, используемых для указания состояния записей адресов во время процесса разрешения имен.
  
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

## <a name="members"></a>Members

 **cFlags**
  
> Число определенных MAPI флажки в списке.
    
 **ulFlags**
  
> Массив флаги, который предоставляет сведения о состоянии операцию разрешения имени для получателя. Можно задать следующие флажки:
    
MAPI_AMBIGUOUS 
  
> Получатель была устранена, но не уникальный идентификатор. Другие контейнеры адресной книги не рекомендуется для устранения этой получателя. 
    
MAPI_RESOLVED 
  
> Получатель была устранена в уникальный идентификатор. Другие контейнеры адресной книги не рекомендуется для устранения этой получателя. 
    
MAPI_UNRESOLVED 
  
> Операция не была устранена. Другие контейнеры адресной книги должны пытаться разрешить этому получателю.
    
## <a name="remarks"></a>Замечания

Структура **FLAGLIST** используется в качестве параметра [IABContainer::ResolveNames](iabcontainer-resolvenames.md). Каждого из получателей будет включен в структуру [ADRLIST](adrlist.md) . Как контейнер адресной книги предпринимается попытка разрешить каждого получателя, соответствующей записи в структуре **FLAGLIST** устанавливает соответствующий флаг. Все записи в структуре **FLAGLIST** , в том же порядке, как записи в структуре **ADRLIST** . Это позволяет легко связать параметр флага с получателем. 
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Структуры MAPI](mapi-structures.md)

