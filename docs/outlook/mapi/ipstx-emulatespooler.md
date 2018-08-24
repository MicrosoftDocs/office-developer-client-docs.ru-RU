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
ms.openlocfilehash: 079b54757cfcd5c9b38365abc5a6d901e2b06724
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580721"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает локальное хранилище для эмуляции диспетчера протокола Outlook очереди исходящих сообщений на сервере.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in] Присвойте этому параметру значение True, если локального хранилища эмуляции очереди; Задайте его значение False, если это не так. 
    
## <a name="remarks"></a>Замечания

Локальное хранилище вызывает **IPSTX::EmulateSpooler** , чтобы выступать в роли Outlook протокола диспетчера, очередь сообщений в очереди исходящих сообщений для внутреннего сервера (например, MSN сервера или сервера AOL) для обработки. Моделирование диспетчер очереди во время синхронизации, хранилище вызывает эти два метода: 
  
1. **[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** для получения очереди исходящих сообщений в хранилище. Этот метод выполнен успешно только в том случае, если хранилище является эмуляции диспетчера протокола Outlook. 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** для обеспечения безопасности единственного доступа к сообщению в очереди исходящих перед отправкой на сервер. Этот метод выполнен успешно только в том случае, если хранилище является эмуляции диспетчера протокола Outlook. После отправки сообщения, хранилище вызывает этот метод еще раз, чтобы освободить единственного доступа к нему. 
    
> [!NOTE]
> Начиная с Outlook 2002 диспетчера протокола Outlook заменены диспетчер очереди MAPI и стала ответственность за исходящих сообщений буферизация фоновых серверов. 
  
## <a name="see-also"></a>См. также



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

