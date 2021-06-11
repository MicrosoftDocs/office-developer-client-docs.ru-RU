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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331390"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) структур, используемых для описания свойства типа PT_MV_I8. 
  
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

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество значений в массиве, на который указывает член **lpli.** 
    
 **lpli**
  
> Указатель на массив **LARGE_INTEGER** структур с значениями в составе. 
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о PT_MV_18 см. [в списке типов свойств.](property-types.md)
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

