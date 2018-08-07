---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8044eb6647e6f437c87bb4d8b021c62ea15f606
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809901"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Относится к**: Outlook 
  
Эта структура используется с [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a>Members

 **ulSize**
  
> Размер структуры.
    
 **ulFlags**
  
> Флаг, указывающий тип синхронизации. Оно должно быть одно из следующих значений:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Отправьте сообщение на сервер (не в настоящее время).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Применить изменения иерархии на сервере.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Изменения иерархии по запросу с сервера.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Применить изменения сообщения на сервер.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Извлечь изменения сообщений с сервера.  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |Синхронизация была инициирована пользователем и должен быть более высокий приоритет.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Рекомендуется выполнять синхронизацию только заголовки и текст сообщений не полный.  <br/> |
   
 **psesSync**
  
> [IN] Указатель на сеанс MAPI.
    
 **punkCallBack**
  
> [IN] Указатель на интерфейс для предоставления хода выполнения. Его можно использовать для запроса интерфейс для [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> [OUT] Событие, возникающее после завершения потока, который был только что создан. Указатель должен быть допустимый, так как он содержит события.
    
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

