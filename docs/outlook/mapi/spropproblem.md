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
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407776"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В этой статье описывается ошибка, связанная с операцией, включающей в себя свойство.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a>"Участники"

 **улиндекс**
  
> Индекс в массиве тегов свойств.
    
 **улпроптаг**
  
> Тег Property для свойства с ошибкой.
    
 **SCODE**
  
> Значение ошибки, описывающее проблему со свойством. Это значение может быть любым значением [SCODE](scode.md) MAPI. 
    
## <a name="remarks"></a>Примечания

Массив структур **спроппроблем** возвращается из следующих методов: 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Структура **спроппроблем** содержит значение ошибки **SCODE** , полученное в результате операции, пытающейся изменить или удалить свойство MAPI. 
  
Дополнительные сведения о том, как структура **спроппроблем** работает с ошибками, связанными со свойствами, в разделе [свойства MAPI с именем](mapi-named-properties.md). 
  
## <a name="see-also"></a>См. также



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[Структуры MAPI](mapi-structures.md)

