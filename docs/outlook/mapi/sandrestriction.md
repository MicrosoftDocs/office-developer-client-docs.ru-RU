---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438885"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение **AND,** которое используется для присоединить группу ограничений с помощью логической **операции AND.** 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>"Участники"

 **cRes**
  
> Количество ограничений поиска в массиве, на который указывает **член lpRes.** 
    
 **lpRes**
  
> Указатель на массив структур [SRestriction,](srestriction.md) которые будут объединены с логической операцией **AND.** 
    
## <a name="remarks"></a>Примечания

Результат **SAndRestriction имеет** true, если все его ограничения для всех его child-ограничений оцениваются как TRUE. Если для какого-либо из ограничений имеется уровень FALSE, то имеется false. 
  
Описание типов ограничений, их сборки и пример кода см. в [описании ограничений.](about-restrictions.md)
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

