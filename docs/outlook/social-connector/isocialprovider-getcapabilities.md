---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Получает строку, которая описывает возможности поставщика.
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812729"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Получает строку, которая описывает возможности поставщика.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Параметры

_результат_
  
> [out] XML-строка, которая представляет возможности поставщика Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Замечания

XML-строка возвращаемый _результат_ должен соответствовать требованиям определение схемы для элемента **capabilities** , как определено в XML-схему для расширений поставщика OSC. 
  
Поставщик должен возвращать строку _результатов_ для включения последующие вызовы от OSC к поставщику для правильной работы. 
  
## <a name="see-also"></a>См. также

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

