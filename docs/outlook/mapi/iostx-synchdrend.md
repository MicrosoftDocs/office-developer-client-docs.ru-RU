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
ms.openlocfilehash: a40d4e62a930219a738c7b431f3d2192007c3d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591333"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Завершает синхронизации для заголовка сообщения.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Параметры

 _pprog_
  
> [in] Интерфейс **[IMAPIProgress](imapiprogressiunknown.md)** для синхронизации перемещения или копирования сообщения. В разделе mapidefs.h для определения типа **LPMAPIPROGRESS**. 
    
## <a name="remarks"></a>Замечания

После **[IOSTX::SyncBeg](iostx-syncbeg.md)** локального хранилища вводит [загрузить состояние заголовка сообщения](download-message-header-state.md). Клиент загружает элемент полного сообщения (как *pmsgFull* в **[HDRSYNC](hdrsync.md)** ). Если это выполнена успешно, клиент также задается *ulFlags* в **HDRSYNC** **HSF_OK**. После **IOSTX::SyncHdrEnd**Outlook проверяет результат в **HDRSYNC** и использует *pprog* и данные в **HDRSYNC** для обновления заголовка локального сообщения. 
  
Возвращает состояние, в котором он находился до предыдущей **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** локального хранилища. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[��������� MAPI](mapi-constants.md)

