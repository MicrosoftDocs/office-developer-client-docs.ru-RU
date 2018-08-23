---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bc0ae6d69db6077c17d2efa66d04a5366f2395a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585572"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур [идентификатор GUID](guid.md) , используемые для описания свойства типа PT_MV_CLSID. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Число значений в массиве, на который указывает член **lpguid** . 
    
 **lpguid**
  
> Указатель на массив структур **идентификатор GUID** , который содержит значения идентификатор класса. 
    
## <a name="remarks"></a>Замечания

Дополнительные сведения о PT_MV_CLSID увидеть [Список типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[ИДЕНТИФИКАТОР GUID](guid.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

