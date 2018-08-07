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
ms.openlocfilehash: bae750e7e940bc1417b3d225c9c81129e9da77b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812331"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Относится к**: Outlook 
  
Сопоставляет перечисляемые целое значение отображаемое имя для этого значения. 
  
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

## <a name="members"></a>Members

 **pszDisplayName**
  
> Строка, содержащая отображаемое имя для значения, указанного в элементе **nVal** . 
    
 **nVal**
  
> Значение перечисления в поле отображаемое имя, на который указывает член **pszDisplayName** . 
    
## <a name="remarks"></a>Замечания

Когда пользователь выбирает отображаемое имя из формы, соответствующее значение перечисления имя хранится с помощью реализации интерфейса [IMAPIProp](imapipropiunknown.md) , связанный с формой. 
  
## <a name="see-also"></a>См. также



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

