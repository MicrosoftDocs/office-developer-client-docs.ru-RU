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
ms.openlocfilehash: 261a59e628320f384deeb760ba71c9c0386cfde6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576045"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения о синхронизации заголовок сообщения во время [загрузки состояния заголовок сообщения](download-message-header-state.md).
  
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
  
- [out] Сведения о текущем заголовок сообщения в локальном хранилище.
    
 _feidPar_
  
- [out] Идентификатор записи для родительской папки сообщения элемента.
    
 _pstmReserved_
  
- [] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
 _ulFlags_
  
- [in] Флаги для изменения поведения:
    
- HSF_LOCAL
    
  - [in] Все элементы находится в том же локальном хранилище, как заголовок элемента.
    
- HSF_COPYDESTRUCTIVE
    
  -  [in] Оптимизация операций внутренней копии. Это может привести к потере данных. Должно иметь значение **HSF_LOCAL** . 
    
- HSF_OK
    
  - [in] Заголовок синхронизация прошла успешно. Устанавливается клиентом после скачивания информации с сервера.
    
     _pmsgFull_
    
  - [in] Полное сообщение элемента, включая заголовок сообщения загружаются с сервера. В разделе mapidefs.h для определения типа **LPMESSAGE**. 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[Константы MAPI](mapi-constants.md)
  
[FEID](feid.md)

