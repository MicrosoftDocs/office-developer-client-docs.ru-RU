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
ms.openlocfilehash: 7108a7e42e9b54e069d8d420283c1ebad3367830
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812751"
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

