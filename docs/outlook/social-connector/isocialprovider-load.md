---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Инициализирует поставщик Outlook social Connector (OSC).
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285762"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Инициализирует поставщик Outlook social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Parameters

_socialProviderInterfaceVersion_
  
> [in] Версия интерфейсов поставщика OSC, ожидаемых osc.
    
_LanguageTag_
  
> [in] Языковой тег Целевой группы интернет-инженерии (IETF), определенный [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) и [[RFC4647],](https://www.ietf.org/rfc/rfc4647.txt)представляет текущий язык Outlook пользовательского интерфейса.
    
## <a name="remarks"></a>Примечания

Формат версии для  _параметра socialProviderInterfaceVersion_  _— X_. _xxxx_, где  _X_ является основной версией,  _а xxxx_ — второстепенной версией OSC. В Office 2013 г. проверьте, является ли основная версия 15. 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

