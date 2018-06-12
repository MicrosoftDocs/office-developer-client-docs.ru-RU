---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Создает копию перечислителя, с помощью же ограничения времени, но установки курсора в начало перечислитель.
ms.openlocfilehash: 51503be2091fa01da6f636bf6944274068617f05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807705"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

Создает копию перечислителя, с помощью же ограничения времени, но установки курсора в начало перечислитель.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>Parameters

_ppclone_
  
> [out] A указателя копию интерфейс [IEnumFBBlock](ienumfbblock.md) . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|E_OUTOFMEMORY  <br/> |Не хватает памяти для создания копии.  <br/> |
   
## <a name="see-also"></a>См. также

- [Константы (занятости API)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

