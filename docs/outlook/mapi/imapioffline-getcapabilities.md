---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433376"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает условия, для которых автономный объект поддерживает вызовы.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Параметры

 _pulCapablities_
  
> [out] Битоваяmas следующих флагов возможностей:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> Автономный объект может предоставлять автономные уведомления.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> Автономный объект может предоставлять интерактивные уведомления.
    
## <a name="remarks"></a>Примечания

Открыв автономный объект с помощью **[HrOpenOfflineObj,](hropenofflineobj.md)** клиент может запросить у [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) указатель на интерфейс **IMAPIOffline** и вызвать **IMAPIOffline::GetCapabilities,** чтобы узнать, поддерживаются ли объектом вызовы. Затем клиент может настроить вызовы с помощью **IMAPIOfflineMgr.**
  
Обратите внимание, что в зависимости от почтового сервера для автономного объекта объект, поддерживаюющий вызовы для работы в сети, не обязательно поддерживает вызовы для работы в автономном режиме.
  
Кроме того, обратите внимание, что, хотя автономный объект может поддерживать функции вызова для изменений, кроме сетевых или автономных, API автономного состояния поддерживает только изменения в сети или автономном режиме, и клиенты должны проверять только такие возможности.
  
## <a name="see-also"></a>См. также



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[��������� MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

