---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404857"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отменяет вызовы для автономного объекта.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Флаги для отмены вызова. Поддерживается только MAPIOFFLINE_UNADVISE_DEFAULT значение.
    
 _ulAdviseToken_
  
> [in] Маркер рекомендации, идентифицирует отменяемую регистрацию вызова. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов был успешным. Этот вызов должен вернуться S_OK.
    
## <a name="remarks"></a>Примечания

Удаляет регистрацию обратного вызова, связанного с  *ulAdviseToken,*  возвращаемого по предварительному вызову **[в IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Вызывает **объект IMAPIOfflineMgr** для выпуска ссылки на **[объект IMAPIOfflineNotify,](imapiofflinenotifyiunknown.md)** связанный с *ulAdviseToken.* 
  
## <a name="see-also"></a>См. также



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Константы MAPI](mapi-constants.md)

