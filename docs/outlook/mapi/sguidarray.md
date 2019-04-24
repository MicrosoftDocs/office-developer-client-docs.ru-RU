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
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339216"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив структуры [GUID](guid.md) , который используется для описания свойства типа пт_мв_клсид. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a>Members

 **Квалуес**
  
> Количество значений в массиве, на которое указывает элемент **лпгуид** . 
    
 **лпгуид**
  
> Указатель на массив структур **GUID** , который содержит значения идентификатора класса. 
    
## <a name="remarks"></a>Комментарии

Дополнительные сведения о ПТ_МВ_КЛСИД приведены в разделе [список типов свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

