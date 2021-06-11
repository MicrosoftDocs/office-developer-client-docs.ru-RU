---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435910"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив строковых значений, используемых для описания свойства типа PT_MV_STRING8.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество значений в массиве, на который указывает **член lppszA.** 
    
 **lppszA**
  
> Указатель на массив из 8-битных 8-битных строк символов.
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о PT_MV_STRING8 см. [в списке типов свойств.](property-types.md)
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

