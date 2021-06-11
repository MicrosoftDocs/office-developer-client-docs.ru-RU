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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Подготавливает локальный магазин для синхронизации в определенном состоянии и извлекает необходимые сведения для репликации.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parameters

 _uiSync_
  
>  [in] Состояние, в которое будет входить локальный магазин. Ниже приводится список идентифицирований состояния: 
    
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
  
>  [in]/[out] Указатель на структуру данных, соответствующую введите состояние. 
    
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

Клиент вызывает **[IOSTX::SetSyncResult,](iostx-setsyncresult.md)** чтобы установить результат синхронизации, а затем вызывает **[IOSTX::SyncEnd,](iostx-syncend.md)** чтобы закончить это состояние. Клиент должен вызвать **[IOSTX::SyncEnd](iostx-syncend.md)** для каждого вызова **в IOSTX::SyncBeg,** чтобы определить, было ли состояние успешно реплицировано. После того как это будет определено, Outlook можно приступить к очистке своего внутреннего состояния. 
  
Большинство из этих структур содержат сведения [out]/[in], что позволяет Outlook передавать сведения клиенту, а клиенту передавать информацию Outlook. Когда клиент вызывает **IOSTX::SyncBeg,** Outlook выделяет структуру данных для данного состояния и инициализирует ее с информацией для этого состояния. Это сведения о [выходе]. Находясь в состоянии, клиент обновляет соответствующую структуру данных для этого состояния. Это [ в] информации. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

