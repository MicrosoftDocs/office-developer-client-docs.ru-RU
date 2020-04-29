---
title: исоЦиалпровидерлоад
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Инициализирует поставщик Outlook Social Connector (OSC).
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285762"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Инициализирует поставщик Outlook Social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Параметры

_соЦиалпровидеринтерфацеверсион_
  
> возврата Версия интерфейсов поставщика OSC, ожидаемых для OSC.
    
_лангуажетаг_
  
> возврата Тег языка IETF, определяемый [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) и [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), который представляет текущий язык пользовательского интерфейса Outlook.
    
## <a name="remarks"></a>Примечания

Формат версии для параметра _соЦиалпровидеринтерфацеверсион_ — _X_. _XXXX_, где _X_ — это основная версия, а _XXXX_ — вспомогательная версия OSC. Для Office 2013 проверьте наличие основной версии 15. 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

