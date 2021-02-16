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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434146"
---
# <a name="upreade"></a>UPREADE

**Относится к**: Outlook 2013 | Outlook 2016 
  
Расширенные сведения о загрузке состояния чтения элемента во время [отправки состояния чтения.](upload-read-status-state.md)
  
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
  
>  [out]/[in] Flags to determine the appropriate behavior during the upload. 
    
  - UPR_ASSOC
    
    - [out] Элемент скрыт.
    
  - UPR_READ
    
    - [out] Состояние чтения элемента было изменено.
    
  - UPR_OK
    
    - [in] Отправка прошла успешно. Клиент устанавливает это после отправки сведений на сервер.
    
  - UPR_COMMIT
    
    - [in] Теперь загрузите состояние чтения элемента вместо того, чтобы [](upload-table-state.md) ждать окончания состояния отправки таблицы для пакетной обработки более одного элемента. 
    
_skey_
  
> [out] Исходный ключ элемента.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)
- [UPREAD](upread.md)

