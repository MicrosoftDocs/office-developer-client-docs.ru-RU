---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- функция xlopertoxloper12 [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807385"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Процедура преобразования используются для преобразования из старого **XLOPER** новые **XLOPER12**.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameters

_pxloper_ (**LPXLOPER**)
  
Указатель на источник **XLOPER** преобразование. 
  
_pxloper12_ (**LPXLOPER12**)
  
Указатель на целевой **XLOPER12** наличия преобразованное значение. 
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

**Значение TRUE,** Если преобразование выполнено успешно, **значение FALSE** в противном случае. 
  
## <a name="remarks"></a>Замечания

В зависимости от типа **XLOPER**эта функция выделяет новый буфер памяти для преобразованные значения, которые являются направлена в целевом **XLOPER12**. Вызывающий объект несет ответственность за освобождает память, связанных с копией ли преобразование будет успешно; Можно использовать **FreeXLOper12T** или можно выполнить с помощью **свободного**.
  
В случае сбоя преобразования вызывающего освободить память, не требуется.
  
В общем случае преобразование из любого **XLOPER** **XLOPER12** невозможно. С другой стороны преобразование из **XLOPER12** **XLOPER** может завершиться неудачно **XLOPER12** содержит массив или ссылку слишком большого размера или строка, слишком много времени для **XLOPER** для хранения. 
  
**XLOPER** Строки байтов ASCII преобразуются в строки Юникода **XLOPER12** Юникод, чтобы зависит от языкового стандарта. 
  
### <a name="example"></a>Пример

Просмотрите файл `\SAMPLES\FRAMEWRK\FRAMEWRK.C` код для этой функции. 
  

