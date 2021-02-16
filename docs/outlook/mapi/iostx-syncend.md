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
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439578"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Завершает синхронизацию в текущем состоянии и завершает это состояние.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Примечания

Клиент должен вызывать **IOSTX::SyncEnd для** каждого вызова [IOSTX::SyncBeg.](iostx-syncbeg.md) Соответствующая структура данных содержит сведения о том, успешно ли завершил клиент текущее состояние, чтобы Outlook можно было очистить его внутреннее состояние.
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

