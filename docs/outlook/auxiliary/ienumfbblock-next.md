---
title: Иенумфбблоккнекст
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Получает следующее указанное количество блоков данных о занятости в перечислении.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422140"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Получает следующее указанное количество блоков данных о занятости в перечислении.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иенумфбблокк](ienumfbblock.md).
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>Параметры

_celt_
  
> возврата Количество блоков данных о занятости в *пблк* , которое требуется получить. 
    
_пблк_
  
> возврата Указатель на массив блоков занятости. Размер массива размещается в параметре *celt* . Запрошенные блоки сведений о занятости возвращаются в этом массиве. 
    
_пкфетч_
  
> вышли Количество блоков сведений о доступности, фактически возвращенных в *пблк* . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Возвращено запрошенное число блоков.  <br/> |
|S_FALSE  <br/> |Запрошенное число блоков не было возвращено.  <br/> |
   
## <a name="see-also"></a>См. также

- [Константы (API сведений о доступности)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

