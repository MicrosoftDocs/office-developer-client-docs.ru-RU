---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- функция xloper12toxloper [Excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422910"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Процедура преобразования, используемая для преобразования из **нового XLOPER12** в старый **XLOPER.**
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parameters

_pxloper12_ **(LPXLOPER12)**
  
Указатель на исходный **XLOPER12** для преобразования. 
  
_pxloper_ **(LPXLOPER)**
  
Указатель на целевой **XLOPER,** чтобы содержать преобразованные значения. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

**TRUE,** если преобразование удалось, **FALSE** в противном случае. 
  
## <a name="remarks"></a>Примечания

В зависимости от типа **XLOPER12** эта функция выделяет новый буфер памяти для преобразованных значений, которые указываются в целевом **XLOPER**. Вызывающий отвечает за то, чтобы освободить любую память, связанную с копией, если преобразование успешно; **FreeXLOperT** можно использовать или сделать это напрямую с помощью **бесплатного**.
  
Если преобразование не удается, вызываемой не требуется освободить память.
  
Преобразование **из XLOPER12** в **XLOPER** может привести к сбою, если **XLOPER12** содержит слишком большой массив или ссылку, слишком длинную для **XLOPER.** 
  
**XLOPER12** Строки с широкими символами юникода преобразуются в строки **byte XLOPER** ASCII, зависящие от локальности. 
  
**XLOPER12** **xltypeInt** — это 32-битный подписанный ряд, в то время как **xltypeInt** **XLOPER** — это 16-битный подписанный ряд. Если количество комплектуемого **XLOPER12** превышает предельный уровень количества **XLOPER,** он преобразуется в двухместный 8-кет и возвращается в **XLOPER** типа **xltypeNum.** Это единственный случай, когда эта функция изменяет тип преобразованного **XLOPER.**
  
### <a name="example"></a>Пример

См.  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` файл кода для этой функции. 
  
## <a name="see-also"></a>См. также

- [Функции в библиотеке платформы](functions-in-the-framework-library.md)

