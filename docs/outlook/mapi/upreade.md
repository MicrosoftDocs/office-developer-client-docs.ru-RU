---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338866"
---
# <a name="upreade"></a>UPREADE

**Область применения**: Outlook 2013 | Outlook 2016 
  
Расширенные сведения для отправки состояния чтения элемента во время [отправки](upload-read-status-state.md)состояния прочтения.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Элементы

_ulFlags_
  
>  [out]/[in] флаги для определения надлежащего поведения при отправке. 
    
  - UPR_ASSOC
    
    - вышли Элемент скрыт.
    
  - UPR_READ
    
    - вышли Состояние чтения элемента изменилось.
    
  - UPR_OK
    
    - возврата Отправка выполнена успешно. Клиент устанавливает это после отправки информации на сервер.
    
  - UPR_COMMIT
    
    - возврата Отправить состояние чтения элемента теперь, не дожидаясь окончания [состояния таблицы отправки](upload-table-state.md) , в пакетную обработку нескольких элементов. 
    
_скэй_
  
> вышли Ключ источника элемента.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)
- [UPREAD](upread.md)

