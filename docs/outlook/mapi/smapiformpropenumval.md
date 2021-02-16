---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435413"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сопозовет измеримые integer-значения с отображаемым именем для этого значения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>"Участники"

 **pszDisplayName**
  
> Строка, содержаная отображаемого имени для значения, указанного в **члене nVal.** 
    
 **nVal**
  
> Значение enumeration для отображаемого имени, на которое указывает **член pszDisplayName.** 
    
## <a name="remarks"></a>Примечания

Когда пользователь выбирает отображаемую имя из формы, соответствующее значение его нумерации сохраняется с помощью реализации интерфейса [IMAPIProp,](imapipropiunknown.md) связанной с формой. 
  
## <a name="see-also"></a>См. также



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

