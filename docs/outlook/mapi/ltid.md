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
ms.openlocfilehash: 29dd2e3b47d0f43df7824274d2fdcc4f7f16eeb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569857"
---
# <a name="ltid"></a>LTID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Универсальный длинный идентификатор термина объекта в хранилище Outlook.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Members

 _Идентификатор GUID_
  
- [out] Идентификатор GUID сервера, создавшее этот объект.
    
 _globcnt_
  
- [out] 6-байтовое уникальный номер, идентифицирующий объекта в хранилище Outlook.
    
 _wLevel_
  
- [out] Уровень иерархии идентификатор записи для Exchange избранные общей папки.
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[FEID](feid.md)

