---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Возвращает идентификатор GUID, который представляет уникальный идентификатор для социальных сетей.
ms.openlocfilehash: 5ff10d51fab03c3bca3eead52848088f2cd80bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812748"
---
# <a name="isocialprovidersocialnetworkguid"></a>ISocialProvider::SocialNetworkGuid

Возвращает идентификатор GUID, который представляет уникальный идентификатор для социальных сетей.
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a>Значение свойства

Указатель на значение GUID, который представляет уникальный идентификатор для социальных сетей.
  
## <a name="remarks"></a>Замечания

Идентификатор GUID должны быть постоянными и не должно изменяться даже при изменении версии поставщика.
  
## <a name="see-also"></a>См. также

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

