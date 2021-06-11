---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419438"
---
# <a name="ltid"></a>LTID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Общий долгосрочный ID объекта в Outlook магазине.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Элементы

 _guid_
  
- [вышел] GUID сервера, создав объект.
    
 _globcnt_
  
- [вышел] Уникальный номер 6-byte, который идентифицирует объект в Outlook магазине.
    
 _wLevel_
  
- [вышел] Уровень иерархии ID записи для Exchange избранной публичной папки.
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[FEID](feid.md)

