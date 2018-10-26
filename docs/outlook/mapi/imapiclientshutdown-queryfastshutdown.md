---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 784a2f497811ba7c4ba0abf260ff32fde75de76a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584935"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запросы в подсистеме MAPI для быстрое завершение работы поддерживают, предоставленные загруженных поставщики MAPI.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Подсистема MAPI поддерживает быстрое завершение работы клиента MAPI.
    
MAPI_E_NO_SUPPORT
  
> Поставщик MAPI не поддерживает быстрое завершение работы клиента MAPI.
    
## <a name="remarks"></a>Замечания

Поддерживает ли подсистемы MAPI клиенту MAPI быстрое завершение работы зависит от параметры реестра Windows и поведение по умолчанию для быстрое завершение работы клиента MAPI. Он также зависит от возможность загрузки поставщики MAPI поддерживает быстрое завершение работы. Для получения дополнительных сведений см [Fast параметры завершения работы пользователя](fast-shutdown-user-options.md).
  
## <a name="see-also"></a>См. также



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

