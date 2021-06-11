---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 78ccf72f17ec350d77f2d22d0e6d2fa7c3d97543
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432872"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает результат синхронизации.
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>Parameters

 _hrSync_
  
>  [in] Результат синхронизации. 
    
## <a name="remarks"></a>Примечания

Позвоните **в IOSTX::SetSyncResult** перед вызовом **IOSTX::SyncEnd** для информирования локального магазина о результатах синхронизации. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[Константы MAPI](mapi-constants.md)

