---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Инициализирует поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 172595db8d9467f22a80c8caf0e3444250826aaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812731"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Инициализирует поставщика Outlook Social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Parameters

_socialProviderInterfaceVersion_
  
> [in] Версия интерфейсы поставщика OSC, ожидаемый OSC.
    
_languageTag_
  
> [in] Тег языка IETF Internet Engineering Task Force (), определенные в [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) и [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), представляющий текущий язык пользовательского интерфейса Outlook.
    
## <a name="remarks"></a>Замечания

Версия формата для параметра _socialProviderInterfaceVersion_ составляет _X_. _xxxx_, где _X_ — это основной версии и _xxxx_ — это дополнительный номер версии OSC. Office 2013 Проверьте основной номер версии, 15. 
  
## <a name="see-also"></a>См. также

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

