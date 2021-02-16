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
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406859"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив одной или более [структур SPropProblem.](spropproblem.md) 
  
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

## <a name="members"></a>"Участники"

 **cProblem**
  
> Количество структур [SPropProblem](spropproblem.md) в массиве, указанных **членом aProblem.** 
    
 **aProblem**
  
> Массив структур **SPropProblem,** каждый из которых описывает ошибку свойства. 
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о том, как структуры **SPropProblem** и **SPropProblemArray** работают с ошибками, связанными со свойствами, см. в полезных свойствах [MAPI.](mapi-named-properties.md) 
  
## <a name="see-also"></a>См. также



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[Структуры MAPI](mapi-structures.md)

