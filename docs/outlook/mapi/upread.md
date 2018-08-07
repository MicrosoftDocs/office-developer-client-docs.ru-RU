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
ms.openlocfilehash: fa3c0b90a64c90a7c854cb22ac75438fa5fca23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812565"
---
# <a name="upread"></a>UPREAD

  
  
**Относится к**: Outlook 
  
Информация для загрузки состояние чтения элементов во время [Отправить прочитать состояние состояние](upload-read-status-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Members

 _pupre_
  
>  [out] Вектор **[UPREADE](upreade.md)** записей. 
    
 _централизованной_
  
>  [out] Число записей **UPREADE** . 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[��������� MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)

