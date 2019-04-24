---
title: Иосткссинчдренд
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
description: 'Дата последнего изменения: 03 июля, 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332188"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Завершает синхронизацию для заголовка сообщения.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Параметры

 _ппрог_
  
> возврата Интерфейс **[IMAPIProgress](imapiprogressiunknown.md)** для синхронизации перемещенных или скопированных сообщений. Определение типа **лпмапипрогресс**можно найти в файле MAPIDEFS. h. 
    
## <a name="remarks"></a>Комментарии

После **[иосткс:: синкбег](iostx-syncbeg.md)**, локальное хранилище вводит [состояние загрузки сообщения](download-message-header-state.md). Клиент загружает полный элемент сообщения (как *пмсгфулл* в **[хдрсинк](hdrsync.md)** ). В случае успеха клиент также устанавливает *ulFlags* в **хдрсинк** как **хсф_ок**. После **иосткс:: синчдренд**Outlook проверяет результат в **хдрсинк** и использует *ппрог* и информацию в **хдрсинк** для обновления заголовка локального сообщения. 
  
Локальное хранилище возвращается в состояние, в котором оно находилось до предшествующего **[иосткс:: синчдрбег](iostx-synchdrbeg.md)**. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)

