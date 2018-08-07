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
ms.openlocfilehash: 62c18ac609547563ad0e98cbd914866e05888ac8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812577"
---
# <a name="uptble"></a>UPTBLE

**Относится к**: Outlook 
  
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

