---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait"
Last modified: April 26, 2021
ms.openlocfilehash: 43a88507cbfc23b3b842f51e69eb4bd791bcfda8
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062020"
---
# <a name="imapiinitmonitorbeginwait"></a>IMAPIInitMonitor::BeginWait
  
**Применяется к**: Outlook 2016 | 2019
  
Начните ожидание инициализации MAPI или указанного числа миллисекунд, которые должны сойти. Это возвращает интерфейс IMAPIWaitResult, который должен иметь **IMAPIWaitResult::End,** чтобы инициировать ожидание. Это позволяет звонячему управлять тем, какой поток заблокирован во время ожидания.

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a>Параметры
_timeout_
>[in] Количество миллисекунд, которые нужно ждать инициализации MAPI, можно задать бесконечное ожидание инициализации навсегда.

_ppResult_
>[вышел] Указатель для получения нового интерфейса ожидания.

## <a name="return-value"></a>Возвращаемое значение
S_OK
>Успешно началась операция ожидания.

E_OUTOFMEMORY
>Для создания нового объекта не хватило памяти

## <a name="remarks"></a>Примечания
Этот API предоставил вызываемого пользователя интерфейс (безопасный для потоков), который можно использовать для инициализации блокировки для инициализации MAPI. Это позволяет потребителю отпугивать наилучшее ожидание для их приложения.   Поведение вызова IMAPIWaitResult:::End идентично вызову IMAPIInitMonitor::Wait.

## <a name="see-also"></a>См. также

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
