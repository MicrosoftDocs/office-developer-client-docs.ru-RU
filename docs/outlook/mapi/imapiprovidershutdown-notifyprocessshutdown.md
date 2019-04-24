---
title: Имапипровидершутдовннотифипроцессшутдовн
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326392"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает поставщику MAPI, что клиент MAPI планирует выполнить быстрое завершение работы, чтобы поставщик мог выполнять действия для предотвращения потери данных.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Поставщик MAPI принимает действия по предотвращению потери данных при завершении работы клиента MAPI.
    
## <a name="see-also"></a>См. также



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

