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
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344543"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение **** , которое используется для применения логической операции **Not** к ограничению. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a>Members

 **Улресервед**
  
> [in] ���������������; ������ ���� ����� ����.
    
 **Лпрес**
  
> Указатель на структуру [срестриктион](srestriction.md) , описывающую ограничение, которое необходимо присоединить к логическому оператору **Not** . 
    
## <a name="remarks"></a>Комментарии

Более подробную информацию о структуре **снотрестриктион** можно узнать в статье [ограничения](about-restrictions.md). 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

