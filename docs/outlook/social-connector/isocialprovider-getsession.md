---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Получает интерфейс ISocialSession.
ms.openlocfilehash: afa13bddd5cbbc53081f6ae7ddcc1671d1c40303
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419550"
---
# <a name="isocialprovidergetsession"></a>ISocialProvider::GetSession

Получает [интерфейс ISocialSession.](isocialsessioniunknown.md) 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Параметры

_session_
  
> Интерфейс **ISocialSession**. 
    
## <a name="remarks"></a>Комментарии

В Outlook social Connector (OSC) используется **интерфейс ISocialSession** для входа в социальную сеть. 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

