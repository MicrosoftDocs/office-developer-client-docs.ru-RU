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
ms.openlocfilehash: fa8b84e7baed74bda25ec1b20bd79fb121a838fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587574"
---
# <a name="upmsg"></a>UPMSG

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Сведения для отправки элемента Outlook во время [отправки сообщения состояния](upload-message-state.md).
  
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

## <a name="members"></a>Members

 _ulFlags_
  
> [out] и [in] флаги для определения соответствующего поведения во время загрузки. 
    
  - UPM_ASSOC
    
    - [out] Элемент связан.
    
  - UPM_NEW
    
    - [out] Новый элемент. 
    
  - UPM_MOV
    
    - [out] Переместить элемент здесь.
    
  - UPM_MOD_PROPS
    
    - [out] Изменения свойств элемента.
    
  - UPM_HEADER
    
    - [out] Элемент — это заголовок сообщения.
    
  - UPM_OK
    
    - [in] Отправка прошла успешно. Клиент устанавливает это после отправки информации на сервер.
    
  - UPM_MOVED
    
    - [in] Элемент успешно перемещен.
    
  - UPM_COMMIT
    
    - [in] Теперь сохранить отправка состояний.
    
  - UPM_DELETE
    
    - [in] Теперь удалите элемент.
    
  - UPM_SAVE
    
    - [in] Сохраните изменения в элемент.
    
_pmsg_
  
> [out] Открытие элементов объекта. В разделе mapidefs.h для определения типа **LPMESSAGE**. 
    
_meid_
  
> [out] Идентификатор элемента записи.
    
_binReserved1_
  
> [in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_binReserved2_
  
> [in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_feid_
  
> [out] Идентификатор записи исходной папки, если элемент был перемещен.
    
_binChg_
  
> [out] Изменение ключа элемента назначения, если элемент был перемещен. В разделе mapidefs.h для определения типа **SBinary**. 
    
_binPcl_
  
> [out] Изменить список элемент назначения, если элемент был перемещен. В разделе mapidefs.h для определения типа **SBinary**. 
    
_skeySrc_
  
> [out] Ключ исходного элемента источника, если элемент был перемещен.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [��������� MAPI](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

