---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408686"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает на намерение клиента MAPI немедленно выйти из клиентского процесса.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Подсистема MAPI указала загруженным поставщикам MAPI, что клиент MAPI немедленно выходит из сети, и поставщики MAPI готовы к выходу клиента.
    
MAPI_E_NO_SUPPORT
  
> Подсистема MAPI не поддерживает быстрое завершение работы клиента.
    
## <a name="remarks"></a>Примечания

Чтобы избежать потери данных при быстром отключении клиента MAPI, клиенты MAPI должны вызывать методы [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) и **IMAPIClientShutdown::D oFastShutdown** на основе результата S_OK, возвращенного подсистемой MAPI в методе [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) Дополнительные сведения см. в лучших [методиках быстрого завершения работы.](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>См. также



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

