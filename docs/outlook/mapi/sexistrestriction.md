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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение EXISTS, используемое для проверки существования определенного свойства в виде столбца в таблице. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
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
  
> Резервирования должно быть равно нулю. 
    
 **улпроптаг**
  
> Тег свойства, определяющий столбец, который необходимо проверить на существование в каждой строке.
    
 **ulReserved2**
  
> Резервирования должно быть равно нулю.
    
## <a name="remarks"></a>Примечания

Ограничение EXISTS используется для обеспечения осмысленных результатов для других типов ограничений, включающих в себя свойства, такие как ограничения свойств и контента. Если ограничение, включающее свойство, передается в [IMAPITable:: restrict](imapitable-restrict.md) или [IMAPITable:: FindRow](imapitable-findrow.md) , а свойство не существует, результаты ограничения не определены. Создавая **ограничение,** которое присоединяется к ограничению свойств с ограничением EXISTS, вызывающий абонент может гарантировать точный результат. 
  
Ограничения EXISTS не могут использоваться с свойствами вложенных объектов, имеющими тип PT_OBJECT. 
  
Более подробную информацию о структуре **сексистрестриктион** можно узнать в статье [ограничения](about-restrictions.md). 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

