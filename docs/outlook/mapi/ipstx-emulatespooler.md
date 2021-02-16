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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает локальное хранилище для эмуляции диспетчера протоколов Outlook для перенаправления исходяющих сообщений на сервер.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in] Установите для этого параметра true, если локальное хранилище должно эмулировать пул; Если нет, установите для него false. 
    
## <a name="remarks"></a>Примечания

Локальное хранилище вызывает **IPSTX::EmulateSpooler,** чтобы выступать в качестве диспетчера протоколов Outlook, перенаправление сообщений из исходяющей очереди на тыловой сервер (например, сервер MSN или сервер AOL) для обработки. После эмуляции пула во время синхронизации хранилище вызывает эти два метода: 
  
1. **[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** для получения очереди исходяющих сообщений в магазине. Этот метод успешно используется, только если хранилище эмулирует диспетчер протоколов Outlook. 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** для защиты единственного доступа к сообщению в исходявой очереди перед отправкой на сервер. Этот метод успешно используется, только если хранилище эмулирует диспетчер протоколов Outlook. После отправки сообщения магазин снова вызывает этот метод, чтобы освободить к нему единственный доступ. 
    
> [!NOTE]
> Начиная с Outlook 2002 диспетчер протоколов Outlook заменил диспетчер протокола MAPI и стал отвечать за перенаправление исходяющих сообщений на серверы. 
  
## <a name="see-also"></a>См. также



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

