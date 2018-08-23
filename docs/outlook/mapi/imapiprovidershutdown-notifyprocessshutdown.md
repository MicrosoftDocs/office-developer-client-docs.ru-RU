---
title: IMAPIProviderShutdownNotifyProcessShutdown
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
ms.openlocfilehash: 251359a98f89c88e707e4f705bd94b1f30b32cbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592054"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает поставщика MAPI, что клиент MAPI требуется выполнить быстрое завершение работы, чтобы поставщик можно выполнять действия, чтобы предотвратить потерю данных.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Поставщик MAPI занимает действия, чтобы предотвратить потерю данных, если клиент MAPI завершает работу.
    
## <a name="see-also"></a>См. также



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Завершение работы клиента в MAPI](client-shutdown-in-mapi.md)

