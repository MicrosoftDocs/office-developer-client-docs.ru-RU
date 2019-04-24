---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Получает автоматически настроенный интерфейс ISocialSession.
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285781"
---
# <a name="isocialprovidergetautoconfiguredsession"></a>ISocialProvider::GetAutoConfiguredSession

Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md). 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Параметры

_session_
  
> Интерфейс **ISocialSession**. 
    
## <a name="remarks"></a>Комментарии

Для возвращенного интерфейса **ISocialSession** автоматически выполняется вход в сеть на основании метода поставщика. 
  
Поставщик должен возвратить ошибку OSC_E_NOT_IMPLEMENTED, если социальная сеть не поддерживает автоматическую настройку. Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

