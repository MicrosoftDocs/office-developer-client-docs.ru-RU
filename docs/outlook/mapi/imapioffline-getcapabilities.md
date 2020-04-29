---
title: имапиоффлинежеткапабилитиес
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
  
Получает условия, для которых в автономном объекте поддерживаются обратные вызовы.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Параметры

 _пулкапаблитиес_
  
> вышли Битовая маска следующих флагов возможностей:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> Автономный объект способен предоставлять уведомления в автономном режиме.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> Автономный объект способен предоставлять интерактивные уведомления.
    
## <a name="remarks"></a>Примечания

При открытии автономного объекта с помощью **[хропеноффлинеобж](hropenofflineobj.md)** клиент может запросить [имапиоффлинемгр](imapiofflinemgrimapioffline.md) , чтобы получить указатель на интерфейс **имапиоффлине** , и вызвать **имапиоффлине::** GetObject, чтобы узнать, какие обратные вызовы поддерживаются объектом. После этого клиент может выбрать настройку обратных вызовов с помощью **имапиоффлинемгр**.
  
Обратите внимание, что в зависимости от почтового сервера для автономного объекта объект, который поддерживает обратные вызовы для подключения к сети, не обязательно поддерживает обратные вызовы при переходе в автономный режим.
  
Обратите внимание, что в то время как автономный объект может поддерживать обратные вызовы для изменений, отличных от Online и offline, API автономного состояния поддерживает только изменения в сети и вне сети, а клиенты должны проверять только такие возможности.
  
## <a name="see-also"></a>См. также



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[��������� MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

