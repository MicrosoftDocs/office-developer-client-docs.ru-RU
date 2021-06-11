---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Получает строку, описываемую возможностями поставщика.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408105"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Получает строку, описываемую возможностями поставщика.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameters

_result_
  
> [вышел] Строка XML, которая представляет возможности поставщика Outlook social Connector (OSC).
    
## <a name="remarks"></a>Примечания

Строка _XML_ возвращаемого результата должна соответствовать  определению схемы элемента возможностей, как определено в схеме XML для extensibility поставщика OSC. 
  
Поставщик должен вернуть строку  _результатов,_ чтобы обеспечить правильную работу последующих вызовов из OSC к поставщику. 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

