---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1b262ba9c83e9890719f716a373c566be172ae73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572454"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит массив значений валюты, которые используются для описания свойства типа PT_MV_CURRENCY. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Число значений в массиве, на который указывает член **lpcur** . 
    
 **lpcur**
  
> Указатель на массив структур [валюты](currency.md) , которые содержат денежными значениями. 
    
## <a name="remarks"></a>Замечания

Сведения о PT_MV_CURRENCY содержатся [Типы списка свойств](property-types.md). 
  
## <a name="see-also"></a>См. также



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

