---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Получает следующее указанное количество блоков бесплатных и загруженных данных в переумериях.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422140"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Получает следующее указанное количество блоков бесплатных и загруженных данных в переумериях.
  
## <a name="quick-info"></a>Краткие сведения

См. [iEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>Parameters

_кельт_
  
> [in] Количество бесплатных и загруженных блоков данных  *в pblk*  для получения. 
    
_pblk_
  
> [in] Указатель на массив бесплатных и занятых блоков. Массиву выделяется размер *кельта.* Запрашиваемая бесплатная/занятая блоки возвращаются в этом массиве. 
    
_pcfetch_
  
> [вышел] Количество бесплатных и занятых блоков фактически возвращается  *в pblk*  . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Возвращено запрашиваемого количества блоков.  <br/> |
|S_FALSE  <br/> |Запрашиваемая часть блоков не возвращена.  <br/> |
   
## <a name="see-also"></a>См. также

- [Константы (API free/busy)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

