---
title: imapiinitmonitor-wait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.Wait
api_type:
- COM
ms.assetid: ed566cae-35a2-4716-817b-54d1ba6825c6
description: IMAPIAMonitor::Wait
Last modified: April 26, 2021
ms.openlocfilehash: ee46a2744e67804c9dfdac8d7512db1d7b07f8ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062013"
---
# <a name="imapiinitmonitorwait"></a>IMAPIInitMonitor::Wait
  
**Применяется к**: Outlook 2013 | Outlook 2016 | 2019
  
Инициирует вызов BLOCKING в этом потоке, который возвращается либо после инициализации указанного числа миллисекунд, либо при инициализации MAPI. INFINITE можно использовать для бесконечного ожидания.

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a>Parameters
_timeout_
> [in] Количество миллисекунд, которые нужно ждать инициализации MAPI, можно передать INFINITE (0xFFFFFFFF), чтобы ждать вечно.

## <a name="return-value"></a>Возвращаемое значение

S_OK
> MapI успешно инициализирована.

HRESULT_FROM_WIN32 (ERROR_TIMEOUT)
> Если дано бесконечное время ожидания, это указывает на то, что MAPI не инициализировался в течение этого периода.

## <a name="remarks"></a>Примечания
  
## <a name="see-also"></a>См. также

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
