---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6c5480a8f5e008c01c7ab8141317f5f19547ab10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414769"
---
# <a name="mapioffline_notify"></a>MAPIOFFLINE_NOTIFY

**Относится к**: Outlook 2013 | Outlook 2016 
  
Это уведомление об изменении состояния подключения. Он указывает измененную часть состояния подключения, старое и новое состояние подключения.
  
## <a name="quick-info"></a>Краткие сведения

См. **[IMAPIOfflineNotify.](imapiofflinenotifyiunknown.md)** 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a>"Участники"

 _ulSize_
  
> Размер **MAPIOFFLINE_NOTIFY** структуры. 
    
 _NotifyType_
  
> Тип уведомления. Обратите внимание, что поддерживается только уведомление об изменении состояния подключения; Поддерживаются только такие значения:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Маркер, определенный клиентом **[](mapioffline_adviseinfo.md)** в структуре MAPIOFFLINE_ADVISEINFO **[IMAPIOfflineMgr::Advise.](imapiofflinemgr-advise.md)** 
    
 _ulMask_
  
> Измененная часть состояния подключения. Единственное поддерживаемые значения — MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulStateOld_
  
> Старое состояние подключения. Поддерживаются только такие значения:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> Новое состояние подключения. Поддерживаются только такие значения:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>Примечания

API автономного состояния поддерживает только уведомления об изменениях в сети или автономном режиме. Перед проверкой фактического изменения клиент должен проверить, возвращает ли Outlook следующие значения:
  
1.  *NotifyType*  имеет значение MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE или MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. В этом случае клиент может предположить, что изменение является изменением состояния подключения, а *сведения* — структурой *StateChange.* 
    
2.  *ulMask*  имеет значение MAPIOFFLINE_STATE_OFFLINE_MASK. В этом случае клиент может предположить, что это изменение сетевого/автономного состояния подключения, и продолжить изучение *ulStateOld* и *ulStateNew.* 
    
Вполне возможно, что Outlook извеирует клиента о других изменениях, которые не поддерживаются. В таких случаях *NotifyType* не будет одним из трех значений, которые были заранее задеклины, или *ulMask* не будет MAPIOFFLINE_STATE_OFFLINE_MASK, и клиент должен игнорировать остальные данные в *сведениях.* 
  
## <a name="see-also"></a>См. также

- [Об API автономного режима](about-the-offline-state-api.md)  
- [��������� MAPI](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

