---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406782"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив значений времени, которые используются для описания свойства типа PT_MV_SYSTIME.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a>"Участники"

 **квалуес**
  
> Количество значений в массиве, на которое указывает элемент **лпфт** . 
    
 **лпфт**
  
> Указатель на массив структуры [fileTime](filetime.md) , который содержит значения времени. 
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о PT_MV_SYSTIME приведены в разделе [список типов свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

