---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 26, 2021
ms.openlocfilehash: 6870c8fa0de51b626662c58b2c8c300c3a4d806e
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062027"
---
# <a name="imapiinitmonitorisinitialized"></a>IMAPIInitMonitor::IsInitialized
  
**Применяется к**: Outlook 2013 | Outlook 2016 | 2019
  
Запрашивает MAPI, чтобы определить, инициализирована ли она в процессе вызова.

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a>Параметры
Нет

## <a name="return-value"></a>Возвращаемое значение
BoOL, указывающее текущее состояние инициализации MAPI, значение TRUE означает, что MAPI инициализирован и доступен для использования, в то время как значение FALSE означает, что MAPI является текущим и не готово к потреблению.

## <a name="remarks"></a>Примечания
Это можно использовать для определения готовности MAPI к применению, например, если приложение хотело что-то сделать, только если MAPI уже инициализирован, это может быть полезной проверкой фоновой задачи, чтобы предотвратить затраты на закрепление MAPI для необязательных работ.

## <a name="see-also"></a>См. также

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
