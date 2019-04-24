---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361168"
---
# <a name="slongarray"></a>SLongArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив типов ДЛИННых значений, которые используются для описания свойства типа ПТ_МВ_ЛОНГ. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Members

 **Квалуес**
  
> Количество значений в массиве, на которое указывает элемент **ЛПЛ** . 
    
 **ЛПЛ**
  
> Указатель на массив ДЛИННых значений.
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о ПТ_МВ_ЛОНГ приведены в разделе [список типов свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

