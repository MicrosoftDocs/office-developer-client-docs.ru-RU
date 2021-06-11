---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Возвращает строку, представляюную номер версии поставщика для этой социальной сети.
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438276"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Возвращает строку, представляюную номер версии поставщика для этой социальной сети. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Значение свойства

Строка с номером версии поставщика.
  
## <a name="remarks"></a>Примечания

Строка версии должна использовать  _MajorVersion_. _Формат MinorVersion_ (например, 1.4730). 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

