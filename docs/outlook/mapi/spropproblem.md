---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7c19cce33ec351a5627870782ebb4fe509a98be2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573287"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит описание ошибки, которые относятся к операции, включающие использование свойства.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a>Members

 **ulIndex**
  
> Индекс массива тегов свойств.
    
 **ulPropTag**
  
> Тег свойства для свойства, которое содержит ошибки.
    
 **SCODE**
  
> Значение ошибки, описанием проблемы со свойством. Это значение может быть любое значение MAPI [SCODE](scode.md) . 
    
## <a name="remarks"></a>Замечания

Массив структур **SPropProblem** возвращается из следующих методов: 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Структура **SPropProblem** содержит значение **SCODE** ошибки, результатом операции, изменение или удаление свойства MAPI. 
  
Дополнительные сведения о работе структура **SPropProblem** при этом возникают ошибки, связанные с свойства в разделе [Свойства с именем MAPI](mapi-named-properties.md). 
  
## <a name="see-also"></a>См. также



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[Структуры MAPI](mapi-structures.md)

