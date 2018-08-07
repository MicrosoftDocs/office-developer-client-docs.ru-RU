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
ms.openlocfilehash: 07305f712fd925b206ce18a32f8f5a24f199ccbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809461"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**Относится к**: Outlook 
  
Информирует хранилище локального сообщений, что синхронизация является запуск.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Флаги для определения соответствующего поведения при синхронизации. Outlook использует эти флаги в каждом состояние конечного автомата репликации, чтобы определить сведения, которые следует предоставить для клиента. Например если клиент передает **SYNC_ONLY_ASSOCIATED**, Outlook будет возвращать только данные, связанные с элементами связанные (или скрытых). 
    
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[��������� MAPI](mapi-constants.md)

