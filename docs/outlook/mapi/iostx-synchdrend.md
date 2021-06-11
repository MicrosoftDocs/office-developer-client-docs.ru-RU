---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Последнее изменение: 03 июля 2012 г.'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432774"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Завершается синхронизация для заглавного сообщения.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Parameters

 _pprog_
  
> [in] **[Интерфейс IMAPIProgress](imapiprogressiunknown.md)** для синхронизации перемещений или копирования сообщений. См. mapidefs.h для определения типа **LPMAPIPROGRESS**. 
    
## <a name="remarks"></a>Примечания

После **[IOSTX::SyncBeg](iostx-syncbeg.md)** локальный магазин вводит состояние заглавного сообщения [для скачивания.](download-message-header-state.md) Клиент загружает полный элемент сообщения (как *pmsgFull* в **[HDRSYNC).](hdrsync.md)** Если это успешно, клиент также задает  *ulFlags*  в **HDRSYNC** как **HSF_OK**. После **IOSTX::SyncHdrEnd** Outlook в **HDRSYNC** и использует *pprog* и сведения **в HDRSYNC** для обновления локального заголовка сообщений. 
  
Локальный магазин возвращается в состояние, в который он был до предыдущего **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

