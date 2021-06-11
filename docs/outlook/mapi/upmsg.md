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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения о загрузке элемента Outlook во время [состояния отправки сообщения.](upload-message-state.md)
  
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
  
> [out]/[in] Флаги для определения соответствующего поведения во время загрузки. 
    
  - UPM_ASSOC
    
    - [вышел] Элемент связан.
    
  - UPM_NEW
    
    - [вышел] Новый элемент. 
    
  - UPM_MOV
    
    - [вышел] Элемент был перемещен сюда.
    
  - UPM_MOD_PROPS
    
    - [вышел] Изменены свойства элемента.
    
  - UPM_HEADER
    
    - [вышел] Элемент — это заглавный элемент сообщения.
    
  - UPM_OK
    
    - [in] Upload успешно. Клиент задает это после отправки сведений на сервер.
    
  - UPM_MOVED
    
    - [in] Элемент был успешно перемещен.
    
  - UPM_COMMIT
    
    - [in] Зафиксировать состояние отправки.
    
  - UPM_DELETE
    
    - [in] Удалите элемент сейчас.
    
  - UPM_SAVE
    
    - [in] Сохранение изменений в элементе.
    
_pmsg_
  
> [вышел] Откройте объект элемента. См. mapidefs.h для определения типа **LPMESSAGE**. 
    
_meid_
  
> [вышел] ID входа элемента.
    
_binReserved1_
  
> [in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_binReserved2_
  
> [in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_feid_
  
> [вышел] Код входа в папку источника, если элемент был перемещен.
    
_binChg_
  
> [вышел] Измените ключ элемента назначения, если элемент был перемещен. См. mapidefs.h для определения **типа SBinary**. 
    
_binPcl_
  
> [вышел] Измените список элемента назначения, если элемент был перемещен. См. mapidefs.h для определения **типа SBinary**. 
    
_skeySrc_
  
> [вышел] Исходный ключ элемента источника, если элемент был перемещен.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

