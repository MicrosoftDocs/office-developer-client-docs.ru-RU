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
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326154"
---
# <a name="upread"></a>UPREAD

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения для отправки состояния чтения элементов во время [отправки](upload-read-status-state.md)состояния прочтения.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Элементы

 _пупре_
  
>  вышли Вектор элементов для **[чтения](upreade.md)** . 
    
 _Центов_
  
>  вышли Количество записей для **чтения** . 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[Константы MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)

