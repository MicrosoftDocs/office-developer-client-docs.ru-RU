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
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418710"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Эта структура используется с [IMAPISync::SynchronizeInBackground.](imapisyncsynchronizeinbackground.md)
  
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

## <a name="members"></a>"Участники"

 **ulSize**
  
> Размер структуры.
    
 **ulFlags**
  
> Флаг, который указывает тип синхронизации. Это должно быть одно из следующих значений:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Отправьте сообщение на сервер (в настоящее время не используется).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Изменение иерархии push-данных на сервере.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Извлеките изменения иерархии с сервера.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Изменение push-сообщений на сервер.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Извлеките изменения сообщений с сервера.  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |Синхронизация была инициирована пользователем и должна иметь более высокий приоритет.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Следует синхронизировать только заглавные и не полные тексты.  <br/> |
   
 **psesSync**
  
> [IN] Указатель на сеанс MAPI.
    
 **аcallBack**
  
> [IN] Указатель на интерфейс, по которому необходимо обеспечить ход выполнения. Его можно использовать для запроса интерфейса [для IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> [OUT] Событие, которое будет происходить после создания только что созданного потока, завершается. Указатель должен быть действительным, так как он будет содержать событие.
    
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

