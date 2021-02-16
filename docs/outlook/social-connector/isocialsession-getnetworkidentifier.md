---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Получает строку, представляюную уникальный идентификатор социальной сети для заданного подключения к социальной сети.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433278"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Получает строку, представляюную уникальный идентификатор социальной сети для заданного подключения к социальной сети. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Параметры

_networkIdentifier_
  
> [out] Строка, содержаная уникальный идентификатор социальной сети.
    
## <a name="remarks"></a>Примечания

Уникальный сетевой идентификатор — это строка, идентифицирует сетевую сеть поставщика Outlook Social Connector (OSC). Этот метод также может возвращать E_NOTIMPL.
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

