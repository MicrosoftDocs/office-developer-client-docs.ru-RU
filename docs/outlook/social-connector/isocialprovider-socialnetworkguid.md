---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Возвращает ИДЕНТИФИКАТОР GUID, который представляет уникальный идентификатор для социальной сети.
ms.openlocfilehash: fc96799ada773cc7260e156d3e2ab8423b73884b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407874"
---
# <a name="isocialprovidersocialnetworkguid"></a>ISocialProvider::SocialNetworkGuid

Возвращает ИДЕНТИФИКАТОР GUID, который представляет уникальный идентификатор для социальной сети.
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a>Значение свойства

Указатель на значение GUID, которое представляет уникальный идентификатор для социальной сети.
  
## <a name="remarks"></a>Примечания

GUID должен быть неуменяемым и не должен изменяться даже при изменении версии поставщика.
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

