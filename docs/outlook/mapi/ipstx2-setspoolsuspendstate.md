---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e988114e8e71ad1f80d20ab0d5a30c37425f5952
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315059"
---
# <a name="ipstx2setspoolsuspendstate"></a>IPSTX2::SetSpoolSuspendState

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает состояние приостановки для диспетчера очереди печати.
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a>Параметры

 _Улстате_
  
> возврата Состояние, в которое задается Диспетчер очереди. Он должен иметь одно из следующих значений:
    
 **SS_ACTIVE**
  
> 
    
 **SS_SUSPENDED**
  
> 
    
## <a name="see-also"></a>См. также



[Константы MAPI](mapi-constants.md)

