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
ms.openlocfilehash: 854e674002953c31c47d56096700dca582ce0a5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812573"
---
# <a name="upreade"></a>UPREADE

**Относится к**: Outlook 
  
Расширенные сведения для загрузки состояние чтения элемента во время [Отправить прочитать состояние состояние](upload-read-status-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Members

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
- [��������� MAPI](mapi-constants.md)
- [UPREAD](upread.md)

