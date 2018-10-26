---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 887c66277b54e2e14c7f67c76b8e9dd4fa8bc719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589233"
---
# <a name="upread"></a>UPREAD

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Информация для загрузки состояние чтения элементов во время [Отправить прочитать состояние состояние](upload-read-status-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Элементы

 _pupre_
  
>  [out] Вектор **[UPREADE](upreade.md)** записей. 
    
 _централизованной_
  
>  [out] Число записей **UPREADE** . 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[Константы MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)

