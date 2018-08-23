---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e601a59a68a3a7d248165d4e573c5abc34d27e2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586468"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит массив двоичных значений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Число значений в массиве, на который указывает член **lpbin** . 
    
 **lpbin**
  
> Указатель на массив структур [SBinary](sbinary.md) , в котором содержатся двоичные значения. 
    
## <a name="remarks"></a>Замечания

Структура **SBinaryArray** используется для описания свойств типа PT_MV_BINARY. 
  
Дополнительные сведения о PT_MV_BINARY увидеть [Список типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

