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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309494"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сопоставляет перечисленное целое число с отображаемым именем для этого значения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>Members

 **Псздисплайнаме**
  
> Строка, содержащая отображаемое имя для значения, указанного в элементе **нвал** . 
    
 **Нвал**
  
> Значение перечисления для отображаемого имени, на которое указывает элемент **псздисплайнаме** . 
    
## <a name="remarks"></a>Замечания

Когда пользователь выбирает отображаемое имя из формы, соответствующее значение перечисления сохраняется с использованием реализации интерфейса [IMAPIProp](imapipropiunknown.md) , связанной с формой. 
  
## <a name="see-also"></a>См. также



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

