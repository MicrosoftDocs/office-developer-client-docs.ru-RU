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
ms.openlocfilehash: ddc61aa42b1087ed5f0ecb7986125ceef27cddce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809462"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**Относится к**: Outlook 
  
Подготавливает локального хранилища для синхронизации в определенное состояние и получает сведения, необходимые для репликации.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Параметры

 _uiSync_
  
>  [in] Состояние, которое будет ввести локального хранилища. Ниже приведен список состояний идентификаторы: 
    
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
  
>  [в] / [out] указатель на структуру данных, соответствующее состоянию для ввода. 
    
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
    
## <a name="remarks"></a>Замечания

Клиент вызывает **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** для установки в результате синхронизации и затем вызывает **[IOSTX::SyncEnd](iostx-syncend.md)** для завершения этого состояния. Клиент должен вызывать **[IOSTX::SyncEnd](iostx-syncend.md)** для каждого вызова **IOSTX::SyncBeg** для определения, была ли успешно реплицирована состояние. После этого определения Outlook можно приступать к Очистка внутреннего состояния. 
  
Большинство этих структур содержат [out] / [in] сведения, и для передачи информации клиент и клиента для передачи сведений об Outlook в Outlook. Когда клиент вызывает **IOSTX::SyncBeg**, Outlook выделяет структуру данных для указанного состояния и инициализирует со сведениями для этого состояния. Это [out] данные. В состоянии, клиент обновляет соответствующие структуры данных для этого состояния. Это [in] сведения. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[��������� MAPI](mapi-constants.md)

