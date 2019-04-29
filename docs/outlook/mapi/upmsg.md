---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427271"
---
# <a name="upmsg"></a>UPMSG

**Относится к**: Outlook 2013 | Outlook 2016 
  
Сведения для отправки элемента Outlook во время [отправки сообщения](upload-message-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a>Элементы

 _ulFlags_
  
> [out]/[in] флаги для определения надлежащего поведения при отправке. 
    
  - UPM_ASSOC
    
    - вышли Связан элемент.
    
  - UPM_NEW
    
    - вышли Новый элемент. 
    
  - UPM_MOV
    
    - вышли Элемент был перемещен здесь.
    
  - UPM_MOD_PROPS
    
    - вышли Изменены свойства элемента.
    
  - UPM_HEADER
    
    - вышли Item — это заголовок сообщения.
    
  - UPM_OK
    
    - возврата Отправка выполнена успешно. Клиент устанавливает это после отправки информации на сервер.
    
  - UPM_MOVED
    
    - возврата Элемент успешно перемещен.
    
  - UPM_COMMIT
    
    - возврата ЗаФиксировать состояние отправки сейчас.
    
  - UPM_DELETE
    
    - возврата Удалить элемент.
    
  - UPM_SAVE
    
    - возврата Сохраните изменения элемента.
    
_ПМСГ_
  
> вышли Открытие объекта Item. Определение типа **лпмессаже**можно найти в файле MAPIDEFS. h. 
    
_MEID_
  
> вышли Идентификатор элемента.
    
_binReserved1_
  
> возврата Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается. 
    
_binReserved2_
  
> возврата Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается. 
    
_feid_
  
> вышли Идентификатор записи исходной папки, если элемент был перемещен.
    
_Бинчг_
  
> вышли Изменение ключа целевого элемента, если элемент был перемещен. Определение типа **сбинари**можно найти в файле MAPIDEFS. h. 
    
_Бинпкл_
  
> вышли Изменение списка конечного элемента, если элемент был перемещен. Определение типа **сбинари**можно найти в файле MAPIDEFS. h. 
    
_Скэйсрк_
  
> вышли Исходный ключ исходного элемента, если элемент был перемещен.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

