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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357843"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив из одной или нескольких структур [спроппроблем](spropproblem.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанные макросы:  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>Members

 **Кпроблем**
  
> Количество структур [спроппроблем](spropproblem.md) в массиве, указанном членом **апроблем** . 
    
 **Апроблем**
  
> Массив структур **спроппроблем** , каждый из которых описывает ошибку свойства. 
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о том, как структуры **спроппроблем** и **спроппроблемаррай** работают с ошибками, связанными со свойствами, в разделе [свойства MAPI с именем](mapi-named-properties.md). 
  
## <a name="see-also"></a>См. также



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[Структуры MAPI](mapi-structures.md)

