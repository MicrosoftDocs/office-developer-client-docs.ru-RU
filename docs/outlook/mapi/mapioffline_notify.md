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
ms.openlocfilehash: b18a4ae4ee25898d1100d9763714e5be21c69fd8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580728"
---
# <a name="mapiofflinenotify"></a>MAPIOFFLINE_NOTIFY

**Относится к**: Outlook 2013 | Outlook 2016 
  
Это уведомление, чтобы внести изменения в состоянии подключения. Он указывает часть состояния подключения, который был изменен, старый состояние подключения и новое состояние подключения.
  
## <a name="quick-info"></a>Краткие сведения

В разделе **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
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

## <a name="members"></a>Members

 _ulSize_
  
> Размер структуры **MAPIOFFLINE_NOTIFY** . 
    
 _NotifyType_
  
> Тип уведомления. Обратите внимание на то, что поддерживается только уведомлений на изменения состояния подключения; поддерживаются только поддерживаемые значения:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Маркер, определенные в клиенте в структуре **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** в **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
    
 _ulMask_
  
> Часть состояния подключения, который был изменен. Поддерживается только значение — MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulStateOld_
  
> Старый состояние подключения. Поддерживаются только поддерживаемые значения:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> Новое состояние подключения. Поддерживаются только поддерживаемые значения:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>Замечания

Автономные состояния API поддерживает только уведомления онлайновом/интерактивном режиме изменения. Клиент должен проверить, что Outlook возвращает следующие значения перед изучением реальное изменение:
  
1.  *NotifyType* имеет значение MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE или MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. В этом случае клиента можно предполагается, что изменения — это изменение состояния подключения и *информация* является структуры *StateChange используется* . 
    
2.  *ulMask* имеет значение MAPIOFFLINE_STATE_OFFLINE_MASK. В этом случае клиент может предполагается, что изменения изменение состояния онлайновом/интерактивном режиме подключения и можно перейти с проверки *ulStateOld* и *ulStateNew* . 
    
Существует возможность, что Outlook уведомляет клиента о других изменений, которые не поддерживаются. В таких случаях одно из трех значений, уже было указано ранее, не приведет к *NotifyType* или *ulMask* не будет MAPIOFFLINE_STATE_OFFLINE_MASK и клиента необходимо игнорировать остальную часть данных в *сведения* . 
  
## <a name="see-also"></a>См. также

- [Сведения об API автономного состояния](about-the-offline-state-api.md)  
- [��������� MAPI](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

