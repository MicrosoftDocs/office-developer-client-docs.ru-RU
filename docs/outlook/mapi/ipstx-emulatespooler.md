---
title: Ипстксемулатеспулер
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
  
Задает локальное хранилище для эмуляции диспетчера протокола Outlook для постановки в очередь исходящих сообщений на сервер.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _Фемулате_
  
>  возврата Установите для этого параметра значение true, если локальное хранилище должно эмулировать Диспетчер очереди печати; Если нет, задайте для него значение false. 
    
## <a name="remarks"></a>Примечания

Локальное хранилище вызывает **ипсткс:: емулатеспулер** для работы в качестве диспетчера протокола Outlook, отправки сообщений из очереди исходящих сообщений на внутренний сервер (например, MSN Server или AOL Server) для обработки. При эмуляции диспетчера очереди во время синхронизации хранилище вызывает следующие два метода: 
  
1. **[IMsgStore:: жетаутгоингкуеуе](imsgstore-getoutgoingqueue.md)** для получения очереди исходящих сообщений в хранилище. Этот метод выполняется только в том случае, если хранилище эмулирует Диспетчер протоколов Outlook. 
    
2. **[IMsgStore:: сетлоккстате](imsgstore-setlockstate.md)** для безопасного доступа к сообщению в исходящей очереди непосредственно перед его отправкой на сервер. Этот метод выполняется только в том случае, если хранилище эмулирует Диспетчер протоколов Outlook. После отправки сообщения хранилище повторно вызывает этот метод, чтобы освободить единственный доступ к нему. 
    
> [!NOTE]
> С момента поЯвления Outlook 2002 Диспетчер протоколов Outlook заменил буфер обмена MAPI и стал ответственным за постановку в очередь исходящих сообщений на внутренние серверы. 
  
## <a name="see-also"></a>См. также



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

