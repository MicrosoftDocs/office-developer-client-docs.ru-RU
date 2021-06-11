---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Ограничивает указанный период времени.
ms.openlocfilehash: e7f7a5d846d13422f9ed79ef26f1b9b0008463f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431948"
---
# <a name="ienumfbblockrestrict"></a>IEnumFBBlock::Restrict

Ограничивает указанный период времени.
  
## <a name="quick-info"></a>Краткие сведения

См. [iEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Parameters

_ftmStart_
  
>  [in] Время начала для ограничения перечня. 
    
_ftmEnd_
  
> [in] Время окончания для ограничения переумерия.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Этот метод также сбрасывает переустановку.
  
## <a name="see-also"></a>См. также

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)  
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

