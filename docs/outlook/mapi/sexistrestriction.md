---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418941"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение на существование, которое используется для проверки того, существует ли определенное свойство в качестве столбца в таблице. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a>"Участники"

 **ulReserved1**
  
> Зарезервировано; должно быть нулевой. 
    
 **ulPropTag**
  
> Тег свойства, определяющий столбец, который необходимо проверить на наличие в каждой строке.
    
 **ulReserved2**
  
> Зарезервировано; должно быть нулевой.
    
## <a name="remarks"></a>Примечания

Ограничение на существование используется для обеспечения значимых результатов для других типов ограничений, которые связаны с свойствами, такими как ограничения свойств и контента. Когда ограничение, в которое входит свойство, передается [в IMAPITable:::Restrict](imapitable-restrict.md) [или IMAPITable::FindRow](imapitable-findrow.md) и свойство не существует, результаты ограничения неопределяются. Создав **ограничение AND,** которое присоединяется к ограничению свойств с ограничением на существование, вызываемой можно гарантировать точные результаты. 
  
Ограничения exist нельзя использовать с свойствами под объекта, которые имеют тип PT_OBJECT. 
  
Дополнительные сведения о структуре **SExistRestriction** см. в дополнительных [сведениях об ограничениях.](about-restrictions.md) 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

