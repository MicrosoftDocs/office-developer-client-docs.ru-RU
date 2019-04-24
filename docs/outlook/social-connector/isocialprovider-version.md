---
title: ИсоЦиалпровидерверсион
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Возвращает строку, представляющую номер версии поставщика для этой социальной сети.
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285387"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Возвращает строку, представляющую номер версии поставщика для этой социальной сети. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Значение свойства

Строка, содержащая номер версии поставщика.
  
## <a name="remarks"></a>Замечания

В строке версии должен использоваться параметр _majorversion_. Формат _minorversion_ (например, 1,4730). 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

