---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Возвращает строку, представляющую номер версии поставщика для этой социальной сети.
ms.openlocfilehash: 5c82df2dc4c052b1a06bcecb16defbb4dee38b18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812734"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Возвращает строку, представляющую номер версии поставщика для этой социальной сети. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Значение свойства

Строка, содержащая номер версии поставщика.
  
## <a name="remarks"></a>Замечания

Строка версии следует использовать _MajorVersion_. Формат _MinorVersion_ (например, 1.4730). 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

