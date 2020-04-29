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
  
Это уведомление об изменении состояния подключения. Он указывает часть состояния подключения, которая изменилась, старое состояние подключения и новое состояние подключения.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)**. 
  
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

 _улсизе_
  
> Размер структуры **MAPIOFFLINE_NOTIFY** . 
    
 _нотифитипе_
  
> Тип уведомления. Обратите внимание, что поддерживается только уведомление при изменении состояния подключения; поддерживаются только следующие значения:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _улклиенттокен_
  
> Маркер, определенный клиентом в структуре **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** в **[Имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)**. 
    
 _улмаск_
  
> Часть состояния подключения, которая изменилась. Единственным поддерживаемым значением является MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _улстатеолд_
  
> Старое состояние подключения. Поддерживаются только следующие значения:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _улстатенев_
  
> Новое состояние подключения. Поддерживаются только следующие значения:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>Примечания

API автономного состояния поддерживает только уведомления об изменениях в Интернете и в автономном режиме. Клиент должен проверить, что Outlook возвращает следующие значения перед изучением фактического изменения:
  
1.  *Нотифитипе* имеет значение MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE или MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. В этом случае клиент может предположить, что изменение является изменением состояния подключения, а *сведения* — с помощью структуры *статечанже* . 
    
2.  *улмаск* имеет значение MAPIOFFLINE_STATE_OFFLINE_MASK. В этом случае клиент может предположить, что изменение является изменением состояния подключения к сети или сети, и может продолжить изучение *улстатеолд* и *улстатенев* . 
    
Outlook может уведомить клиента о других неподдерживаемых изменениях. В таких случаях *нотифитипе* не будет содержать одно из трех значений, упомянутых выше, или *улмаск* не будет MAPIOFFLINE_STATE_OFFLINE_MASK, и клиент должен проигнорировать остальные данные в *info* . 
  
## <a name="see-also"></a>См. также

- [Об API автономного режима](about-the-offline-state-api.md)  
- [��������� MAPI](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

