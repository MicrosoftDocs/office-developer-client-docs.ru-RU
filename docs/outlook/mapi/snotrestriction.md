---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 174da93e7682246565b12c4fc4ffa6d1a9de065c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575065"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описываются ограничения **не** , который используется для применения к ограничению логическая операция **не** . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a>Members

 **ulReserved**
  
> [in] ���������������; ������ ���� ����� ����.
    
 **lpRes**
  
> Указатель на структуру [SRestriction](srestriction.md) , описывающая ограничения, чтобы быть присоединен к логический оператор, который **не** . 
    
## <a name="remarks"></a>Замечания

Дополнительные сведения о структуре **SNotRestriction** [О ограничения](about-restrictions.md)см. 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

