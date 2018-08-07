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
ms.openlocfilehash: f0cf6fa03d8f38b7d160a8747111445cfdac1ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812181"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**Относится к**: Outlook 
  
Описание ограничений Битовая маска, которая используется для выполнения побитовую операцию **и** и проверять этот результат. 
  
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

## <a name="members"></a>Members

 **relBMR**
  
> Оператор сравнения, описывающая способ применения маска, указанных в член **ulMask** тега свойства. Ниже приведены возможные значения: 
    
BMR_EQZ 
  
> Выполните операцию побитовое **и** маски в член **ulMask** со свойством, представленных член **ulPropTag** и тестирования, равное нулю. 
    
BMR_NEZ 
  
> Выполните операцию побитовое **и** маски в член **ulMask** со свойством, представленное член **ulPropTag** и проверить, не равное нулю. 
    
 **ulPropTag**
  
> Свойство tag свойства, к которому применяется Битовая маска.
    
 **ulMask**
  
> Битовую маску, применяемую к свойству, определяемую средством **ulPropTag**.
    
## <a name="remarks"></a>Замечания

Структура **SBitMaskRestriction** выполняет побитовое операцию **и** с помощью Битовая маска, описанные в член **ulMask** и значение свойства, описанные член **ulPropTag** . Если значение равно нулю, выполняется BMR_EQZ. Если ненулевое значение, то есть, если значение свойства есть по крайней мере один из того же битов задаются в виде **ulMask**, затем BMR_NEZ выполняется.
  
Дополнительные сведения о структуре **SBitMaskRestriction** и ограничения в целом, обратитесь к разделу [О ограничения](about-restrictions.md).
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

