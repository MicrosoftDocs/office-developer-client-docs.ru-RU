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
  
Описывает ограничения **и** ограничения, которые используются для присоединения к группе ограничений с помощью логической операции **и** . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>"Участники"

 **крес**
  
> Число ограничений поиска в массиве, на который указывает элемент **лпрес** . 
    
 **лпрес**
  
> Указатель на массив структур [срестриктион](srestriction.md) , которые будут объединены с логической операцией **and** . 
    
## <a name="remarks"></a>Примечания

Результат **сандрестриктион** имеет значение true, если все его дочерние ограничения оцениваются как true. Имеет значение FALSE, если любое дочернее ограничение имеет значение FALSE. 
  
Описание типов ограничений, их построения и пример кода приведено в разделе [ограничения](about-restrictions.md).
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

