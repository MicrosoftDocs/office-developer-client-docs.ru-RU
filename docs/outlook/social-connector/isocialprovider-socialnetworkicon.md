---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Возвращает массив bytes, который представляет значок для социальной сети.
ms.openlocfilehash: c63d9996d4478c8ce7e46210aae34791bcfe9222
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438689"
---
# <a name="isocialprovidersocialnetworkicon"></a>ISocialProvider::SocialNetworkIcon

Возвращает массив bytes, который представляет значок для социальной сети. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a>Значение свойства

Указатель на структуру, которая указывает массив bytes, содержащий значок для социальной сети.
  
## <a name="remarks"></a>Примечания

Поддерживаемые ресурсы изображений .bmp, .jpeg и .png форматов.
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

