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
ms.openlocfilehash: a07a7737e9b9354514a2d5ac2ec37a393a3cd4e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812343"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Относится к**: Outlook 
  
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

