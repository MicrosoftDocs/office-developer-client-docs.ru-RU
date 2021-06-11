---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438955"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает локальный магазин, чтобы подражать диспетчеру Outlook протоколов, чтобы перенаправление исходяющих сообщений на сервер.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in] Установите этот параметр true, если локальный магазин должен подражать шпалеру; установите его false, если нет. 
    
## <a name="remarks"></a>Примечания

Локальный магазин вызывает **IPSTX::EmulateSpooler,** чтобы выступать в качестве диспетчера протоколов Outlook, выполнив перенаправление сообщений в исходяющей очереди на сервер заднего сервера (например, msN server или AOL server) для обработки. Эмулируя шпалер во время синхронизации, магазин вызывает эти два метода: 
  
1. **[IMsgStore::GetOutgoingQueue,](imsgstore-getoutgoingqueue.md)** чтобы получить исходятую очередь сообщений в магазине. Этот метод успешно используется только в том случае, если магазин эмулирует Outlook Диспетчер протокола. 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** для обеспечения единого доступа к сообщению в исходя из очереди перед отправкой на сервер. Этот метод успешно используется только в том случае, если магазин эмулирует Outlook Диспетчер протокола. После отправки сообщения магазин снова вызывает этот метод, чтобы освободить единственный доступ к нему. 
    
> [!NOTE]
> С Outlook 2002 года диспетчер протокола Outlook spooler MAPI и стал отвечать за перенаправление исходяющих сообщений на серверы заднего конца. 
  
## <a name="see-also"></a>См. также



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

