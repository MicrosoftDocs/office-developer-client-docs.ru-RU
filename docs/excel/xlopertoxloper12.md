---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- функция xlopertoxloper12 [Excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404598"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Процедура преобразования, используемая для преобразования из **старого XLOPER** в **новый XLOPER12.**
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameters

_pxloper_ **(LPXLOPER)**
  
Указатель на исходный **XLOPER** для преобразования. 
  
_pxloper12_ **(LPXLOPER12)**
  
Указатель на целевое **значение XLOPER12,** чтобы содержать преобразованные значения. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

**TRUE,** если преобразование удалось, **FALSE** в противном случае. 
  
## <a name="remarks"></a>Примечания

В зависимости от типа **XLOPER** эта функция выделяет новый буфер памяти для преобразованных значений, которые указываются в целевом **XLOPER12.** Вызывающий отвечает за то, чтобы освободить любую память, связанную с копией, если преобразование успешно; **FreeXLOper12T** можно использовать, или это можно сделать непосредственно с помощью **бесплатно**.
  
Если преобразование не удается, вызываемой не требуется освободить память.
  
Как правило, возможно преобразование **из любого XLOPER** в **XLOPER12.** В отличие от этого, преобразование **из XLOPER12** в **XLOPER** может привести к сбою, если **XLOPER12** содержит слишком большой массив или ссылку, слишком длинную для **XLOPER.** 
  
**XLOPER** Строки byte ASCII преобразуются в строки широкого характера **XLOPER12** Unicode таким образом, что зависят от локальности. 
  
### <a name="example"></a>Пример

См.  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` файл кода для этой функции. 
  

