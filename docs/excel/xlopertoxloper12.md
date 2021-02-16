---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- Функция xlopertoxloper12 [excel 2007]
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
  
Процедура преобразования, используемая для преобразования из **старой XLOPER** в **новую XLOPER12.**
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Параметры

_pxloper_ (**LPXLOPER)**
  
Указатель на исходный **XLOPER** для преобразования. 
  
_pxloper12_ (**LPXLOPER12)**
  
Указатель на целевой **объект XLOPER12,** содержащий преобразованные значения. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

**TRUE,** если преобразование успешно, в противном случае **FALSE.** 
  
## <a name="remarks"></a>Примечания

В зависимости от типа **XLOPER** эта функция выделяет новый буфер памяти для преобразованных значений, на которые указывают целевые **значения XLOPER12.** Если преобразование успешно, вызываемая отвечает за освободить память, связанную с копией; **FreeXLOper12T** можно использовать или сделать это напрямую с помощью **бесплатного.**
  
Если преобразование не удается, вызываемой не требуется освободить память.
  
Как правило, преобразование **из любого XLOPER** в **XLOPER12** возможно. С другой стороны, преобразование **из XLOPER12** в **XLOPER** может привести к сбою, если **XLOPER12** содержит слишком большой массив или ссылку или слишком длинную строку для **XLOPER.** 
  
**XLOPER** Строки byte ASCII преобразуются в строки Юникод с широкими символами **XLOPER12** в зависимости от региональных стандартов. 
  
### <a name="example"></a>Пример

Код этой  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` функции см. в файле. 
  

