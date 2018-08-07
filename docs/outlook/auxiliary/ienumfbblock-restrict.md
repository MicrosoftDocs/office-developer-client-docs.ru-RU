---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Ограничивает число перечисления для заданного периода времени.
ms.openlocfilehash: 6b07fe52a84d6a808ab7400ff3e8982b1cce51ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807702"
---
# <a name="ienumfbblockrestrict"></a>IEnumFBBlock::Restrict

Ограничивает число перечисления для заданного периода времени.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Параметры

_ftmStart_
  
>  [in] Время начала, чтобы ограничить перечисления. 
    
_ftmEnd_
  
> [in] Время окончания для ограничения перечисления.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

Этот метод также восстанавливаются значения по умолчанию перечисления.
  
## <a name="see-also"></a>См. также

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)  
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

