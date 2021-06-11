---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410254"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения для синхронизации загона сообщений во время состояния [заглавного сообщения для скачивания.](download-message-header-state.md)
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a>Элементы

 _pupmsg_
  
- [вышел] Сведения для текущего загона сообщений в локальном магазине.
    
 _feidPar_
  
- [вышел] ID записи для родительской папки элемента сообщения.
    
 _pstmReserved_
  
- [] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
 _ulFlags_
  
- [in] Флаги для изменения поведения:
    
- HSF_LOCAL
    
  - [in] Полный элемент находится в том же локальном хранилище, что и элемент header.
    
- HSF_COPYDESTRUCTIVE
    
  -  [in] Оптимизация внутренних операций копирования. Это может привести к потере данных. **HSF_LOCAL** необходимо установить. 
    
- HSF_OK
    
  - [in] Синхронизация header прошла успешно. Устанавливается клиентом после скачивания информации с сервера.
    
     _pmsgFull_
    
  - [in] Полный элемент сообщения, включая заглавную версию сообщения, загруженную с сервера. См. mapidefs.h для определения типа **LPMESSAGE**. 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[Константы MAPI](mapi-constants.md)
  
[FEID](feid.md)

