---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429616"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив неподписаных значений, используемых для описания свойства типа PT_MV_SHORT.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество значений в массиве, на который указывает **член LPI.** 
    
 **LPI**
  
> Указатель на массив неподписаных неподписаных значений.
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о типах PT_MV_SHORT и других типах свойств см. [в см. в этой области.](property-types.md) 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

