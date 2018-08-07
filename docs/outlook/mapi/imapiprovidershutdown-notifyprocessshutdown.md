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
ms.openlocfilehash: cce98dc630dd9f7fa459ca31d94d012ba9a7fd85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809052"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Относится к**: Outlook 
  
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

