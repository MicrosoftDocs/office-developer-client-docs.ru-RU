---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 443644b66ba9c961992e22dbfc260fe8c48fe1b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809880"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Применимо к**: Outlook 
  
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
- [Об автономных состояний API](about-the-offline-state-api.md) 
- [��������� MAPI](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

