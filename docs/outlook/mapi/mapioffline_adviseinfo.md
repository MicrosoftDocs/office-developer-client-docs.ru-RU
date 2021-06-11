---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420026"
---
# <a name="mapioffline_adviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения **[iMAPIOfflineMgr:::Advise](imapiofflinemgr-advise.md)** для регистрации вызова для автономного объекта. 
  
## <a name="quick-info"></a>Краткие сведения

См. **IMAPIOfflineMgr::Advise**. 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a>"Участники"

_ulSize_: Размер **MAPIOFFLINE_ADVISEINFO**. 
    
_ulClientToken:_ маркер, определенный клиентом о вызове. Это член *ulClientToken* структуры **[](mapioffline_notify.md)** MAPIOFFLINE_NOTIFY **[IMAPIOfflineNotify::Notify.](imapiofflinenotify-notify.md)** 
    
_CallbackType._ Тип вызова.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - Тип вызова по уведомлению. Это единственный поддерживаемый тип вызова.  *pCallback должен*  указывать интерфейс **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_pCallback:_ интерфейс, который можно использовать для вызова. Это реализация **[IMAPIOfflineNotify клиента.](imapiofflinenotifyiunknown.md)** 
    
_ulAdviseTypes_: Типы консультирования, как определено условием для консультирования. Единственный поддерживаемый тип — MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask._ Единственным поддерживаемым состоянием является MAPIOFFLINE_STATE_ALL.
    
## <a name="see-also"></a>См. также

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Об API автономного режима](about-the-offline-state-api.md) 
- [��������� MAPI](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

