---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413355"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сообщает локальному хранилище сообщений о том, что синхронизация вот-вот начнется.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Флаги для определения соответствующего поведения во время синхронизации. Outlook использует эти флаги в каждом состоянии машины состояния репликации для определения сведений, которые он должен предоставить клиенту. Например, если клиент проходит **SYNC_ONLY_ASSOCIATED,** Outlook возвращает только сведения, связанные с связанными (или скрытыми) элементами. 
    
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

