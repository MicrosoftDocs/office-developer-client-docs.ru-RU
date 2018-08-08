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
ms.openlocfilehash: 15e2d5c2aca595c3a06d215cd069c23da3e48125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808997"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**Относится к**: Outlook 
  
Задает текущее состояние автономной объекта в сети или в автономном режиме.
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Изменение поведения этот вызов. Приведены поддерживаемые значения.
    
MAPIOFFLINE_FLAG_BLOCK
  
> Установка _ulFlags_ для этого значения будет блокировать вызов **SetCurrentState** до завершения изменения состояния. По умолчанию переход происходит асинхронно. При переходе отмену асинхронно, все вызовы **SetCurrentState** возвращает **E_PENDING** до завершения изменения. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Задает текущее состояние без блокировки.
    
 _ulMask_
  
> [in] Часть состояния для изменения. Поддерживается только значение — MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulState_
  
> [in] Чтобы изменить на состояние. Оно должно быть одно из следующих двух значений:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _Сохраняются_
  
> Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Состояние объекта автономной успешно изменены.
    
E_PENDING
  
> Это указывает на то асинхронно изменение состояния автономного объекта. Происходит, когда _ulFlags_ задано значение MAPIOFFLINE_FLAG_BLOCK в более ранних вызова **SetCurrentState** , а все последующие вызова **SetCurrentState** возвращает это значение до завершения изменений состояния асинхронной. 
    
## <a name="see-also"></a>См. также



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[��������� MAPI](mapi-constants.md)

