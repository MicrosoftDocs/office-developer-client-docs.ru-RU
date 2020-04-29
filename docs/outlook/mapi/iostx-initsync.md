---
title: иостксинитсинк
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Информирует локальное хранилище сообщений о том, что синхронизация будет запущена.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Флаги для определения надлежащего поведения во время синхронизации. Outlook использует эти флаги в каждом состоянии конечного автомата репликации, чтобы определить сведения, которые он должен предоставить для клиента. Например, если клиент передает **SYNC_ONLY_ASSOCIATED**, Outlook будет возвращать только сведения, относящиеся к связанным (или скрытым) элементам. 
    
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

