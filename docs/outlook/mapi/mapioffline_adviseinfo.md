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
ms.openlocfilehash: 82869fa479ebe8a4d7b1881cec5d5c243b7d7957
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565097"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения о **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** для регистрации обратного вызова для объекта в автономном режиме. 
  
## <a name="quick-info"></a>Краткие сведения

В разделе **IMAPIOfflineMgr::Advise**. 
  
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

## <a name="members"></a>Элементы

_ulSize_: размер **MAPIOFFLINE_ADVISEINFO**. 
    
_ulClientToken_: маркер, определенные в клиента о обратного вызова. Это член *ulClientToken* структуры **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** , переданной в **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**. 
    
_CallbackType_: тип обратного вызова, чтобы сделать.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - Тип обратного вызова является уведомлений. Это единственный поддерживаемый тип обратного вызова.  *pCallback* необходимо указать интерфейс **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_pCallback_: интерфейс для обратного вызова. Это реализация клиента **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_ulAdviseTypes_: типы уведомлений, которые определяются условие с уведомлением о том. Единственным поддерживаемым типом является MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask_: MAPIOFFLINE_STATE_ALL — это единственный поддерживаемый состояние.
    
## <a name="see-also"></a>См. также

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Об API автономного режима](about-the-offline-state-api.md) 
- [Константы MAPI](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

