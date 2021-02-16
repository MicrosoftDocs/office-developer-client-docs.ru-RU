---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ae4497295328155780fc5208d1699169698e02d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411941"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Подготавливает локальное хранилище к синхронизации в определенном состоянии и извлекает необходимые сведения для репликации.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Параметры

 _uiSync_
  
>  [in] Состояние, которое будет вводить локальное хранилище. Ниже приводится список отступов состояния. 
    
LR_SYNC_IDLE
  
> 
    
LR_SYNC
  
> 
    
LR_SYNC_UPLOAD_HIERARCHY
  
> 
    
LR_SYNC_UPLOAD_FOLDER
  
> 
    
LR_SYNC_CONTENTS
  
> 
    
LR_SYNC_UPLOAD_TABLE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_READ
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_DEL
  
> 
    
LR_SYNC_DOWNLOAD_HIERARCHY
  
> 
    
LR_SYNC_DOWNLOAD_TABLE
  
> 
    
 _ppv_
  
>  [in]/[out] Pointer to the data structure corresponding to the state to enter. 
    
[DNHIER](dnhier.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[SYNC](sync.md)
  
> 
    
[SYNCCONT](synccont.md)
  
> 
    
[UPDEL](updel.md)
  
> 
    
[UPDELE](updele.md)
  
> 
    
[UPFLD](upfld.md)
  
> 
    
[UPHIER](uphier.md)
  
> 
    
[UPMOV](upmov.md)
  
> 
    
[UPMSG](upmsg.md)
  
> 
    
[UPREAD](upread.md)
  
> 
    
[UPREADE](upreade.md)
  
> 
    
[UPTBL](uptbl.md)
  
> 
    
[UPTBLE](uptble.md)
  
> 
    
## <a name="remarks"></a>Примечания

Клиент вызывает **[IOSTX::SetSyncResult,](iostx-setsyncresult.md)** чтобы установить результат синхронизации, а затем вызывает **[IOSTX::SyncEnd,](iostx-syncend.md)** чтобы закончить это состояние. Клиент должен вызывать **[IOSTX::SyncEnd](iostx-syncend.md)** для каждого вызова **IOSTX::SyncBeg,** чтобы определить, успешно ли реплицировано состояние. После этого Outlook может начать очищать свое внутреннее состояние. 
  
Большинство из этих структур содержат сведения [out]/[in], что позволяет Outlook передавать данные клиенту, а клиент — в Outlook. Когда клиент вызывает **IOSTX::SyncBeg,** Outlook выделяет структуру данных для заданного состояния и инициализирует ее с информацией для этого состояния. Это сведения о [выходе]. Находясь в состоянии, клиент обновляет соответствующую структуру данных для этого состояния. Это сведения о [в]. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

