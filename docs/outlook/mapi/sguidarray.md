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
ms.openlocfilehash: 553ec17e9caf9bf93278ff139eb94e02e6b48554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19812282"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**Относится к**: Outlook 
  
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



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

