---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421741"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает текущее состояние автономного объекта в режиме online или автономном режиме.
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Изменяет поведение этого вызова. Поддерживаются следующие значения:
    
MAPIOFFLINE_FLAG_BLOCK
  
> Настройка  _ulFlags к_ этому значению блокирует вызов **SetCurrentState** до завершения изменения состояния. По умолчанию переход происходит асинхронно. Когда переход происходит асинхронно, **все** вызовы **SetCurrentState** возвращаются E_PENDING до завершения изменения. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Задает текущее состояние без блокировки.
    
 _ulMask_
  
> [in] Изменение части состояния. Единственное поддерживаемые значения — MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulState_
  
> [in] Состояние, на который необходимо изменить. Это должно быть одно из этих двух значений:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _pReserved_
  
> Этот параметр зарезервирован для Outlook и не поддерживается. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Состояние автономного объекта успешно изменено.
    
E_PENDING
  
> Это означает, что состояние автономного объекта меняется асинхронно. Это происходит, когда  _значение ulFlags_ MAPIOFFLINE_FLAG_BLOCK более ранним вызовом **SetCurrentState,** и любой последующий вызов **SetCurrentState** возвращает это значение до завершения асинхронного изменения состояния. 
    
## <a name="see-also"></a>См. также



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[Константы MAPI](mapi-constants.md)

