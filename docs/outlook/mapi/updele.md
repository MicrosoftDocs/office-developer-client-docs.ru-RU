---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4dd60ffe305d27db2c9118e11cccf692652d0d27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812549"
---
# <a name="updele"></a>UPDELE

**Относится к**: Outlook 
  
Подробные данные для элементов, которые были удалены в локальном хранилище. Эти сведения используются во время [загрузки удалить состояние состояние](upload-delete-status-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
> [out] и [in] флаги для определения соответствующего поведения во время передачи данных.
    
  - UPD_ASSOC
    
    - [out] Элемент связан.
    
  - UPD_MOV
    
    - [out] Элемент был перемещен в работе.
    
  - UPD_OK 
    
    - [in] Отправка прошла успешно. Клиент устанавливает это после отправки информации на сервер.
    
  - UPD_MOVED
    
    - [in] Элемент успешно перемещен.
    
  - UPD_UPDATE
    
    - [in] Пометить исходного элемента, как изменения.
    
  - UPD_COMMIT
    
    - [in] Сохранить теперь состояние передачи (запись в 0).
    
_skey_
  
> [out] Ключ исходного элемента.
    
_dwReserved_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
_binChg_
  
> [out] Изменение ключа назначения элемента, если элемент был перемещен.
    
_binPcl_
  
> [out] Изменение списка элемент назначения, если элемент был перемещен.
    
_skeyDst_
  
> [out] Ключ исходного элемента назначения, если элемент был перемещен.
    
_pupmov_
  
> [out] Сведения о папке назначения Если элемент был перемещен.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md) 
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [��������� MAPI](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

