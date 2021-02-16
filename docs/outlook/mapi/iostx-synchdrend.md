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
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432774"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Завершает синхронизацию для загона сообщения.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Параметры

 _pp де_
  
> [in] **[Интерфейс IMAPIProgress](imapiprogressiunknown.md)** для синхронизации перемещенных или скопированные сообщения. Определение типа **LPMAPIPROGRESS** см. в mapidefs.h. 
    
## <a name="remarks"></a>Примечания

После **[IOSTX::SyncBeg](iostx-syncbeg.md)** локальное хранилище введет состояние [скачивания сообщения в состояние загона.](download-message-header-state.md) Клиент скачивает полный элемент сообщения (как *pmsgFull* в **[HDRSYNC).](hdrsync.md)** Если это успешно, клиент также устанавливает *ulFlags* в **HDRSYNC** как **HSF_OK.** После **IOSTX::SyncHdrEnd** Outlook проверяет результат в **HDRSYNC** и использует  *ppлага*  и сведения в **HDRSYNC** для обновления локального заголовка сообщения. 
  
Локальное хранилище возвращается в состояние до предыдущего **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

