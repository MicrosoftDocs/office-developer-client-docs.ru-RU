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
ms.openlocfilehash: 699e77479e0d09e7549c0d2741d5ba54ecc8ce33
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572034"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Получает условия, для которых обратные вызовы поддерживаются автономной объектом.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Параметры

 _pulCapablities_
  
> [out] Битовая маска флагов следующих возможностей:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> Автономные объект может предоставить автономной уведомлений.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> Автономные объект может предоставить online уведомлений.
    
## <a name="remarks"></a>Замечания

При открытии автономного объекта с помощью **[HrOpenOfflineObj](hropenofflineobj.md)** клиента можно запросить на [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) , чтобы получить указатель на интерфейс **IMAPIOffline** и вызовите **IMAPIOffline::GetCapabilities** , чтобы узнать, поддерживается обратные вызовы с помощью объекта. Клиент затем можно настроить обратных вызовов с помощью **IMAPIOfflineMgr**.
  
Обратите внимание, что в зависимости от почтового сервера для автономного объекта, объект, который поддерживает обратных вызовов для подключение не поддерживает обязательно обратных вызовов для перейти в автономный режим.
  
Также Обратите внимание, что при автономной объекта могут поддерживать обратных вызовов для изменения, отличный от онлайновом/интерактивном режиме, автономного состояния API поддерживает только онлайновом/интерактивном режиме изменения и клиенты должен проверять наличие только такие возможности.
  
## <a name="see-also"></a>См. также



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[��������� MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

