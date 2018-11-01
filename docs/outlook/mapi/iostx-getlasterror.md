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
ms.openlocfilehash: 78ae0f78e154c17f774817238b2083d98a8fb809
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584683"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает расширенные сведения о последней ошибки.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
>  [in] Код ошибки. 
    
 _ulFlags_
  
>  [in] Flags to modify behavior. Это должно быть равно 0. 
    
 _lppMAPIError_
  
>  [out] Указатель на структуру **MAPIERROR** , который содержит дополнительные сведения об ошибке. В разделе mapidefs.h для определения типа **LPMAPIERROR**. 
    
## <a name="see-also"></a>См. также



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

