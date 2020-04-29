---
title: иенумфбблоккскип
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Пропускает указанное количество блоков данных о занятости.
ms.openlocfilehash: cf8ae18b5ed2c24a48d44d9e8d461da7d95054d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425724"
---
# <a name="ienumfbblockskip"></a>IEnumFBBlock::Skip

Пропускает указанное количество блоков данных о занятости.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иенумфбблокк](ienumfbblock.md).
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a>Параметры

_celt_
  
>  возврата Количество пропущенных блоков сведений о занятости. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="see-also"></a>См. также

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)

