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
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436803"
---
# <a name="updel"></a>UPDEL

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения об удаленных в локальном магазине элементов. Эта информация используется во время [состояния удаления загрузки.](upload-delete-status-state.md)
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Элементы

 _pupde_
  
>  [вышел] Вектор [записей UPDELE.](updele.md) 
    
 _cEnt_
  
> [вышел] Количество записей в  *pupde*  . 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[Константы MAPI](mapi-constants.md)

