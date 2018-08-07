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
ms.openlocfilehash: bfc03f7fe573005a235154cf179dcf44bf4abd65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812548"
---
# <a name="updel"></a>UPDEL

  
  
**Относится к**: Outlook 
  
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

