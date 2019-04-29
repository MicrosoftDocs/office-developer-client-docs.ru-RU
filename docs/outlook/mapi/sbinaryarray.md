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
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438290"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив двоичных значений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>Members

 **Квалуес**
  
> Количество значений в массиве, на которое указывает элемент **лпбин** . 
    
 **лпбин**
  
> Указатель на массив структур [сбинари](sbinary.md) , в котором хранятся двоичные значения. 
    
## <a name="remarks"></a>Примечания

Структура **сбинаряррай** используется для описания свойств типа пт_мв_бинари. 
  
Дополнительные сведения о ПТ_МВ_БИНАРИ приведены в разделе [список типов свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

