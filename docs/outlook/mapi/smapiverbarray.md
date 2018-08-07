---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812349"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**Относится к**: Outlook 
  
Содержит массив структур [SMAPIVerb](smapiverb.md) , которые описывают команд MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Связанные макрос:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a>Members

 **cForms**
  
> Число команд в массиве.
    
 **aFormInfo**
  
> Массив команд MAPI.
    
## <a name="remarks"></a>Замечания

Структура **SMAPIVerbArray** передается как параметр в методе [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) . 
  
## <a name="see-also"></a>См. также



[SMAPIVerb](smapiverb.md)


[Структуры MAPI](mapi-structures.md)

