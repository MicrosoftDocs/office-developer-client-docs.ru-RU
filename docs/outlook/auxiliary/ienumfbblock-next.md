---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Получает указанное количество блоков данных о доступности в перечислении.
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807711"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Получает указанное количество блоков данных о доступности в перечислении.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>Parameters

_celt_
  
> [in] Количество данных о доступности блоков *pblk* для извлечения. 
    
_pblk_
  
> [in] Указатель на массив сведений о доступности блоки. Массив, выделяемого размер *celt* . Запрошенный блоки занятости возвращаются в этот массив. 
    
_pcfetch_
  
> [out] Количество блоков сведений о доступности, фактически возвращаемую в *pblk* . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |Запрошенный количество блоков возвращена.  <br/> |
|S_FALSE  <br/> |Запрошенный количество блоков не были возвращены.  <br/> |
   
## <a name="see-also"></a>См. также

- [Константы (занятости API)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

