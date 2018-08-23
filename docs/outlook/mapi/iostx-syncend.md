---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fd5b2ed23eba30cbe861a20c4fd100cb8ea1aeb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568842"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Завершает синхронизации в текущем состоянии и выходе из этого состояния.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Замечания

Клиент должен вызывать **IOSTX::SyncEnd** для каждого вызова [IOSTX::SyncBeg](iostx-syncbeg.md). Соответствующий структура данных содержит сведения, которые указывают ли клиент успешного завершения текущего состояния, Outlook может Очистка внутреннего состояния.
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[��������� MAPI](mapi-constants.md)

