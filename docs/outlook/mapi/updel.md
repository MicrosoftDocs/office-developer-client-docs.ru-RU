---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 057a1ff38ed3809ce03bce8f820f1d16eea7fb46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581127"
---
# <a name="updel"></a>UPDEL

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Сведения для элементов, которые были удалены в локальном хранилище. Эти сведения используются во время [загрузки удалить состояние состояние](upload-delete-status-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Members

 _pupde_
  
>  [out] Вектор [UPDELE](updele.md) записей. 
    
 _централизованной_
  
> [out] Число записей в *pupde* . 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[��������� MAPI](mapi-constants.md)

