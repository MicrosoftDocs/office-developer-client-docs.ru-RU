---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3fd61828cd631c4abc0131da867ca213a3c44d20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812374"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**Относится к**: Outlook 
  
Содержит массив из одного или нескольких структур [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>Members

 **cProblem**
  
> Число структур [SPropProblem](spropproblem.md) в массиве, указанный в параметре члена **aProblem** . 
    
 **aProblem**
  
> Массив структур **SPropProblem** каждого описывает ошибку свойство. 
    
## <a name="remarks"></a>Замечания

Дополнительные сведения о работе структур **SPropProblem** и **SPropProblemArray** при этом возникают ошибки, связанные с свойства в разделе [Свойства с именем MAPI](mapi-named-properties.md). 
  
## <a name="see-also"></a>См. также



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[Структуры MAPI](mapi-structures.md)

