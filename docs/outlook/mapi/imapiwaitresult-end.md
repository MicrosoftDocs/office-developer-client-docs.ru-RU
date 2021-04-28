---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 26, 2021
ms.openlocfilehash: 3432bf3b71fa7e15cb4621d461a8d4bbe962f1ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062034"
---
# <a name="imapiwaitresultend"></a>IMAPIWaitResult::End
  
**Применяется к**: Outlook 2013 | Outlook 2016 | 2019

Инициирует вызов BLOCKING в этом потоке, который возвращается либо после инициализации указанного числа миллисекунд, либо при инициализации MAPI. INFINITE можно использовать для бесконечного ожидания.

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a>Параметры

_timeout_
> [in] Количество миллисекунд для ожидания инициализации MAPI можно передать INFINITE (0xFFFFFFFF), чтобы ждать вечно.

## <a name="return-value"></a>Возвращаемое значение

S_OK
> MAPI успешно инициализирована

HRESULT_FROM_WIN32 (ERROR_TIMEOUT)
> Если дано бесконечное время ожидания, это указывает на то, что MAPI не инициализировался в течение этого периода.

## <a name="remarks"></a>Примечания
Этот API ведет себя точно так же, как [и IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).
  
## <a name="see-also"></a>См. также

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
