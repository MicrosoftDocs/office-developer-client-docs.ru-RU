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
ms.openlocfilehash: fd593b68ef7ca25b1f8ceec613786cdbdd03fd76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579076"
---
# <a name="upreade"></a>UPREADE

**Область применения**: Outlook 2013 | Outlook 2016 
  
Расширенные сведения для загрузки состояние чтения элемента во время [Отправить прочитать состояние состояние](upload-read-status-state.md).
  
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
  
>  [out] и [in] флаги для определения соответствующего поведения во время загрузки. 
    
  - UPR_ASSOC
    
    - [out] Элемент скрыт.
    
  - UPR_READ
    
    - [out] Изменилось состояние чтения элемента.
    
  - UPR_OK
    
    - [in] Отправка прошла успешно. Клиент устанавливает это после отправки информации на сервер.
    
  - UPR_COMMIT
    
    - [in] Отправьте состояние чтения элемента сейчас, вместо ожидания до конца [Отправить состояние таблицы](upload-table-state.md) для пакетной обработки более одного элемента. 
    
_skey_
  
> [out] Ключ исходного элемента.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)
- [UPREAD](upread.md)

