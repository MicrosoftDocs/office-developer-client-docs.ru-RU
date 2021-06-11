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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает условия, для которых вызовы поддерживаются автономным объектом.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Parameters

 _pulCapablities_
  
> [вышел] Битмаска следующих флагов возможностей:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> Автономный объект может предоставлять автономные уведомления.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> Автономный объект может предоставлять уведомления в Интернете.
    
## <a name="remarks"></a>Примечания

При открытии автономного объекта с помощью **[HrOpenOfflineObj](hropenofflineobj.md)** клиент может запросить в [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) указатель на интерфейс **IMAPIOffline** и вызвать **IMAPIOffline::GetCapabilities,** чтобы узнать о вызовах, поддерживаемых объектом. Клиент может настроить вызовы с помощью **IMAPIOfflineMgr.**
  
Обратите внимание, что в зависимости от почтового сервера для автономного объекта объект, поддерживаюющий откаты вызовов для подключения к сети, не обязательно поддерживает вызовы для отключения.
  
Кроме того, обратите внимание, что, хотя автономный объект может поддерживать вызовы для изменений, не в режиме online/offline, API состояния автономного доступа поддерживает только изменения в режиме online/offline, и клиенты должны проверять только такие возможности.
  
## <a name="see-also"></a>См. также



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[��������� MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

