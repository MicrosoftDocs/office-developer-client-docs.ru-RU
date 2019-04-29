---
title: Имапиоффлинесеткуррентстате
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает текущее состояние автономного объекта: Online или offline.
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Изменяет поведение этого вызова. Поддерживаются следующие значения:
    
MAPIOFFLINE_FLAG_BLOCK
  
> Если задать для параметра _ulFlags_ значение this, вызов **сеткуррентстате** будет заблокирован до завершения изменения состояния. По умолчанию переход выполняется асинхронно. Когда происходит асинхронный переход, все вызовы **сеткуррентстате** будут возвращать **е_пендинг** до завершения изменения. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Задает текущее состояние без блокировки.
    
 _Улмаск_
  
> возврата Часть состояния, которую необходимо изменить. Единственное поддерживаемое значение — МАПИОФФЛИНЕ_СТАТЕ_ОФФЛИНЕ_МАСК.
    
 _Улстате_
  
> возврата Состояние, в которое нужно изменить. Оно должно быть одним из следующих двух значений:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _Сохранен_
  
> Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Состояние автономного объекта успешно изменено.
    
Е_ПЕНДИНГ
  
> Это указывает на то, что состояние автономного объекта изменяется асинхронно. Это происходит, когда _ulFlags_ имеет значение мапиоффлине_флаг_блокк в предыдущем вызове **сеткуррентстате** , а все последующие вызовы **сеткуррентстате** будут возвращать это значение до завершения асинхронного изменения состояния. 
    
## <a name="see-also"></a>См. также



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[Константы MAPI](mapi-constants.md)

