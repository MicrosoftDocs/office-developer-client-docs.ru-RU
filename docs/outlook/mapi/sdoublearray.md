---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439270"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив двойных номеров, используемых для описания свойства типа PT_MV_DOUBLE.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество значений в массиве, на который указывает член **lpdbl.** 
    
 **lpdbl**
  
> Указатель на массив двойных значений.
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о PT_MV_DOUBLE см. [в списке типов свойств.](property-types.md)
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

