---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382731"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) структуры, используемые для описания свойства типа PT_MV_I8. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Число значений в массиве, на который указывает член **lpli** . 
    
 **lpli**
  
> Указатель на массив структур **LARGE_INTEGER** , сохраняя значения целое число. 
    
## <a name="remarks"></a>Замечания

Дополнительные сведения о PT_MV_18 увидеть [Список типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

