---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438871"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает на намерение клиента MAPI продолжить завершение работы.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Подсистема MAPI попыталась уведомить загруженных поставщиков MAPI о том, что клиент MAPI будет быстро отключиться.
    
## <a name="remarks"></a>Примечания

Чтобы избежать потери данных при быстром отключении клиента MAPI, клиенты MAPI должны вызывать методы **IMAPIClientShutdown::NotifyProcessShutdown** и [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) на основе результата S_OK, возвращенного подсистемой MAPI в методе [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) Дополнительные сведения см. в лучших [методиках быстрого завершения работы.](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>См. также



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

