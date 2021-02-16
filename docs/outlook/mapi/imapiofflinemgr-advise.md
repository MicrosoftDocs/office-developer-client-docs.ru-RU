---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426921"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Регистрирует клиент для получения вызовов в автономном объекте.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
>  [in] Флаги, которые изменяют поведение. Поддерживается только MAPIOFFLINE_ADVISE_DEFAULT значение. 
    
 _pAdviseInfo_
  
> [in] Сведения о типе вызова, о том, когда необходимо получить вызов, интерфейсе и других сведениях для вызываемого. Он также содержит маркер клиента, который Outlook использует для отправки последующих вызовов уведомлений вызываемому клиенту.
    
 _pulAdviseToken_
  
> [out] Маркер консультации, возвращающийся вызываемому клиенту для последующего отмены обратного вызова для объекта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов был успешным.
    
E_INVALIDARG
  
> Указан недопустимый параметр.
    
E_NOINTERFACE
  
> Не является допустимым интерфейсом вызова, указанным *в pAdviseInfo.* 
    
## <a name="remarks"></a>Примечания

При открытии автономного объекта с помощью **[HrOpenOfflineObj](hropenofflineobj.md)** клиент получает автономный объект, который поддерживает **IMAPIOfflineMgr.** Клиент может проверить виды вызовов, поддерживаемых объектом, с помощью **[IMAPIOffline::GetCapabilities.](imapioffline-getcapabilities.md)** Клиент может определить тип и другие сведения о нужном ему вызове, а затем вызвать **IMAPIOfflineMgr::Advise,** чтобы зарегистрироваться для получения таких вызовов об объекте. 
  
## <a name="see-also"></a>См. также



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[��������� MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

