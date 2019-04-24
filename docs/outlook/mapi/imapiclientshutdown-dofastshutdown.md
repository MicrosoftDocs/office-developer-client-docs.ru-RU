---
title: Имапиклиентшутдовндофастшутдовн
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350906"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает на намерение клиента MAPI немедленно выйти из клиентского процесса.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Подсистема MAPI загрузила поставщика MAPI, что клиент MAPI немедленно выходит из системы, а поставщики MAPI готовы к выходу клиента.
    
МАПИ_Е_НО_СУППОРТ
  
> Подсистема MAPI не поддерживает быстрое завершение работы клиента.
    
## <a name="remarks"></a>Примечания

Чтобы избежать потери данных при быстром завершении работы клиента MAPI, клиенты MAPI должны вызывать методы [метод imapiclientshutdown:: нотифипроцессшутдовн](imapiclientshutdown-notifyprocessshutdown.md) и **метод imapiclientshutdown::D офастшутдовн** на основе результата S_OK, возвращаемОГО подсистемой MAPI в метод [метод imapiclientshutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Для получения дополнительных сведений ознакомьтесь с рекомендациями [по быстроМу завершенИю работы](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>См. также



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

