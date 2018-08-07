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
ms.openlocfilehash: 74a4e299da6c0637c3da70c329569266d43dbd9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809463"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**Относится к**: Outlook 
  
Задает в результате синхронизации.
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>Параметры

 _hrSync_
  
>  [in] В результате синхронизации. 
    
## <a name="remarks"></a>Замечания

Вызовите **IOSTX::SetSyncResult** перед вызовом **IOSTX::SyncEnd** для оповещения локального хранилища в результате синхронизации. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[��������� MAPI](mapi-constants.md)

