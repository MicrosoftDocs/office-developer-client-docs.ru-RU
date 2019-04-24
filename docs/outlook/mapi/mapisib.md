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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270212"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Эта структура используется с [имаписинк:: синчронизеинбаккграунд](imapisyncsynchronizeinbackground.md).
  
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

 **Улсизе**
  
> Размер структуры.
    
 **ulFlags**
  
> Флаг, указывающий тип синхронизации. Он должен иметь одно из следующих значений:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Отправьте сообщение на сервер (в данный момент не используется).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Принудительная отправка изменений иерархии на сервер.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Изменение иерархии по запросу с сервера.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Push-сообщения изменяются на сервер.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Изменение сообщений с сервера.  <br/> |
|СИНК_ОН_ДЕМАНД  <br/> |0x20000000  <br/> |Синхронизация была инициирована пользователем и должна иметь более высокий приоритет.  <br/> |
|СИНК_ГЛОБАЛ_ХЕАДЕРС  <br/> |0x02000000  <br/> |Должны синхронизироваться только заголовки и не полные тексты.  <br/> |
   
 **Псессинк**
  
> ВОЗВРАТА Указатель на сеанс MAPI.
    
 **Пунккаллбакк**
  
> ВОЗВРАТА Указатель на интерфейс, для которого необходимо предоставить ход выполнения. Его можно использовать для запроса интерфейса для [имаписинкпрогресскаллбакк: IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*Фсинкдонивент**
  
> ВЫШЛИ Событие, которое будет происходить при завершении созданного вами потока. Указатель должен быть допустимым, так как он будет содержать событие.
    
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

