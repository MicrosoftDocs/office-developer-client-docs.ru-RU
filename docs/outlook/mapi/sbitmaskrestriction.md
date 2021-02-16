---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424478"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение битовыхmask, которое используется для выполнения по битовых операций **AND** и проверки результата. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a>"Участники"

 **relBMR**
  
> Реляционный оператор, который описывает, как маска, указанная в члене **ulMask,** должна применяться к тегу свойства. Возможные значения: 
    
BMR_EQZ 
  
> Выполните по битовую **операцию AND** маски в члене **ulMask** со свойством, представленным членом **ulPropTag,** и проверьте, равно ли она нулю. 
    
BMR_NEZ 
  
> Выполните по битовую операцию **AND** маски в члене **ulMask** со свойством, представленным членом **ulPropTag,** и проверьте, не равна ли она нулю. 
    
 **ulPropTag**
  
> Тег свойства, к которому применяется битоваяmask.
    
 **ulMask**
  
> Битоваяmask, применяемая к свойству, идентифицированного **ulPropTag.**
    
## <a name="remarks"></a>Примечания

Структура **SBitMaskRestriction** выполняет побитовую операцию **AND,** используя битовуюmask, описанную в члене **ulMask,** и значение свойства, описанное в члене **ulPropTag.** Если результат — ноль, BMR_EQZ удовлетворены. Если он ненулев, то есть, если значение свойства имеет по крайней мере один из тех же битов, установленных как **ulMask,** BMR_NEZ удовлетворены.
  
Дополнительные сведения о структуре **и ограничениях SBitMaskRestriction** в целом см. в сведениях [об ограничениях.](about-restrictions.md)
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

