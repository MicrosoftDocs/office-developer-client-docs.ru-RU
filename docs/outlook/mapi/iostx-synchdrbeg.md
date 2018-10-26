---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2d05592d1fdcdcd53c8b7879f9cdcd432df1a3f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579468"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запускает синхронизацию для заголовка сообщения.
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Параметры

 _cbeid_
  
> [in] Число байт в Идентификаторе запись для сообщения.
    
 _lpeid_
  
> [in] Идентификатор записи сообщения.
    
 _ppv_
  
>  [в] и [out] указатель на структуру **[HDRSYNC](hdrsync.md)** для заголовка сообщения. 
    
## <a name="remarks"></a>Замечания

После **IOSTX::SyncHdrBeg**локального хранилища переходы можно [загрузить состояние заголовка сообщения](download-message-header-state.md). Для клиента Outlook инициализирует структуру **HDRSYNC** с текущее представление заголовок сообщения в хранилище и родительской папки. Клиент затем необходимо загрузить элемента полного сообщения (как *pmsgFull* в **HDRSYNC** ). Если это прошла успешно, клиент также задается *ulFlags* в **HDRSYNC** **HSF_OK**. После **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** Outlook проверяет результат в **HDRSYNC** и использует сведения из **HDRSYNC** для обновления заголовка локального сообщения. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

