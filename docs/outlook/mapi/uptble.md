---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b2523c149d98dacf9ad321a4a443382a39753fd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592341"
---
# <a name="uptble"></a>UPTBLE

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Подробные данные для загрузки содержимого папки во время [загрузки состояния в таблице](upload-table-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a>Members

 _iEntMod_
  
>  [out] Индекс для отслеживания отправки _cEntMod_ число новые или измененные элементы. 
    
 _cEntMod_
  
>  [out] Число новые или измененные элементы в папке. 
    
 _iEntRead_
  
>  [out] Индексирование для отслеживания Отправка число _cEntRead_ чтение элементов. 
    
 _cEntRead_
  
>  [out] Количество чтения элементов в папке. 
    
 _iEntDel_
  
>  [out] Индекс для отслеживания Отправка число _cEntDel_ удаленных элементов. 
    
 _cEntDel_
  
>  [out] Количество удаленных элементов в папке. 
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md) 
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

