---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Получает строку, представляющую идентификатор уникальный социальной сети для подключения к указанной социальных сетей.
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812863"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Получает строку, представляющую идентификатор уникальный социальной сети для подключения к указанной социальных сетей. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Параметры

_networkIdentifier_
  
> [out] Строка, содержащая идентификатор уникальный социальных сетей.
    
## <a name="remarks"></a>Замечания

Уникальные идентификатор — это строка, идентифицирующая социальных сетей поставщика Outlook Social Connector (OSC). Этот метод может также возвращать значение E_NOTIMPL.
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

