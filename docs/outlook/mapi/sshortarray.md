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
ms.openlocfilehash: b684309211bbc008856311158c67864d958c96a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573035"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив целых значений, которые используются для описания свойства типа PT_MV_SHORT.
  
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

## <a name="members"></a>Members

 **cValues**
  
> Число значений в массиве, на который указывает член **строки** . 
    
 **линий на дюйм**
  
> Указатель на массив целых значений.
    
## <a name="remarks"></a>Замечания

Дополнительные сведения о PT_MV_SHORT и других типов свойств можно [Типы свойств](property-types.md). 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

