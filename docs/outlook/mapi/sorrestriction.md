---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345103"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение **** , используемое для применения логической операции **или** к ограничению. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a>Members

 **Крес**
  
> Количество структур в массиве, на которое указывает элемент **лпрес** . 
    
 **Лпрес**
  
> Указатель на структуру [срестриктион](srestriction.md) , описывающую ограничение, которое необходимо присоединить с помощью логической операции **or** . 
    
## <a name="remarks"></a>Комментарии

Более подробную информацию о структуре **соррестриктион** можно узнать в статье [ограничения](about-restrictions.md). 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

