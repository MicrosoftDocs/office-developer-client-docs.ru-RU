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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сведения о синхронизации заголовка сообщения во время [загрузки состояния заголовка сообщения](download-message-header-state.md).
  
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

 _пупмсг_
  
- вышли Сведения о текущем заголовке сообщения в локальном хранилище.
    
 _Феидпар_
  
- вышли Идентификатор записи для родительской папки элемента сообщения.
    
 _pstmReserved_
  
- [] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается. 
    
 _ulFlags_
  
- возврата Флаги для изменения поведения:
    
- HSF_LOCAL
    
  - возврата Полный элемент находится в том же локальном хранилище, что и элемент заголовка.
    
- HSF_COPYDESTRUCTIVE
    
  -  возврата Оптимизируйте внутренние операции копирования. Это может привести к потере данных. Необходимо задать **хсф_локал** . 
    
- HSF_OK
    
  - возврата Синхронизация заГоловков выполнена успешно. Устанавливается клиентом после скачивания информации с сервера.
    
     _Пмсгфулл_
    
  - возврата Полный элемент сообщения, включая заголовок сообщения, загруженный с сервера. Определение типа **лпмессаже**можно найти в файле MAPIDEFS. h. 
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[Константы MAPI](mapi-constants.md)
  
[FEID](feid.md)

