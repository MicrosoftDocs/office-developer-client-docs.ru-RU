---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9c29011ae2e9b59a7a0a38148fa6c5b673fd9590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422301"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает расширенные сведения о последней ошибке.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
>  [in] Код ошибки. 
    
 _ulFlags_
  
>  [in] Flags to modify behavior. Это должно быть 0. 
    
 _lppMAPIError_
  
>  [вышел] Указатель на **структуру MAPIERROR,** которая содержит расширенные сведения об ошибке. См. mapidefs.h для определения типа **LPMAPIERROR**. 
    
## <a name="see-also"></a>См. также



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

