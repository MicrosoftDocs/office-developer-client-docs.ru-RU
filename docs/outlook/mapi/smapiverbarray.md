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
ms.openlocfilehash: 7cba5dce60ce15ddb12776d619143849298aac9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433915"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив [структур SMAPIVerb,](smapiverb.md) описывая глаголы MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Связанный макрос:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a>"Участники"

 **cForms**
  
> Количество глаголов в массиве.
    
 **aFormInfo**
  
> Массив глаголов MAPI.
    
## <a name="remarks"></a>Примечания

Структура **SMAPIVerbArray** передается в качестве параметра в [методе IMAPIFormInfo::CalcVerbSet.](imapiforminfo-calcverbset.md) 
  
## <a name="see-also"></a>См. также



[SMAPIVerb](smapiverb.md)


[Структуры MAPI](mapi-structures.md)

