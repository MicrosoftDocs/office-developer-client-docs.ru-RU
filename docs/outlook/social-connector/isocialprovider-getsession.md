---
title: ИсоЦиалпровидержетсессион
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Получает интерфейс настроенный ISocialSession.
ms.openlocfilehash: afa13bddd5cbbc53081f6ae7ddcc1671d1c40303
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285774"
---
# <a name="isocialprovidergetsession"></a>ISocialProvider::GetSession

Получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) . 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Параметры

_session_
  
> Интерфейс **ISocialSession**. 
    
## <a name="remarks"></a>Комментарии

Outlook Social Connector (OSC) использует интерфейс **настроенный ISocialSession** для входа в социальную сеть. 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

