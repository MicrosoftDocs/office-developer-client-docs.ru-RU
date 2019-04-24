---
title: Имапиклиентшутдовннотифипроцессшутдовн
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351361"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает на намерение клиента MAPI выполнить завершение работы.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Подсистема MAPI попыталась уведомить загруженных поставщиков MAPI о том, что клиент MAPI будет выполнять быстрое завершение работы.
    
## <a name="remarks"></a>Примечания

Чтобы избежать потери данных при быстром завершении работы клиента MAPI, клиенты MAPI должны вызывать методы **метод imapiclientshutdown:: нотифипроцессшутдовн** и [метод imapiclientshutdown::D офастшутдовн](imapiclientshutdown-dofastshutdown.md) на основе результата S_OK, возвращаемОГО подсистемой MAPI в метод [метод imapiclientshutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Для получения дополнительных сведений ознакомьтесь с рекомендациями [по быстроМу завершенИю работы](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>См. также



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

