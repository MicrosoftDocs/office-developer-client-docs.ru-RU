---
title: Иенумфбблоккскип
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: ПроПускает указанное количество блоков данных о занятости.
ms.openlocfilehash: cf8ae18b5ed2c24a48d44d9e8d461da7d95054d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317551"
---
# <a name="ienumfbblockskip"></a>IEnumFBBlock::Skip

ПроПускает указанное количество блоков данных о занятости.
  
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

