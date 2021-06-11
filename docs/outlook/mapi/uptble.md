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
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413842"
---
# <a name="uptble"></a>UPTBLE

**Область применения**: Outlook 2013 | Outlook 2016 
  
Расширенные сведения для загрузки содержимого папки во время [состояния таблицы отправки.](upload-table-state.md)
  
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

## <a name="members"></a>Элементы

 _iEntMod_
  
>  [вышел] Индекс для отслеживания загрузки  _номера cEntMod_ новых или измененных элементов. 
    
 _cEntMod_
  
>  [вышел] Количество новых или измененных элементов в папке. 
    
 _iEntRead_
  
>  [вышел] Индекс для отслеживания загрузки количества элементов _чтения cEntRead._ 
    
 _cEntRead_
  
>  [вышел] Количество элементов чтения в папке. 
    
 _iEntDel_
  
>  [вышел] Индекс для отслеживания загрузки количества _удаленных элементов cEntDel._ 
    
 _cEntDel_
  
>  [вышел] Количество удаленных элементов в папке. 
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md) 
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

