---
title: ИсоЦиалпровидержеткапабилитиес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Получает строку, описывающую возможности поставщика.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285767"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Получает строку, описывающую возможности поставщика.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Параметры

_result_
  
> вышли XML-строка, представляющая возможности поставщика Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Замечания

Возвращаемая XML-строка _результата_ должна соответствовать определению схемы для элемента **capabilities** , как определено в схеме XML для расширения поставщика OSC. 
  
Поставщик должен возвратить строку _результата_ , чтобы обеспечить правильную работу последующих вызовов из OSC для поставщика. 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

