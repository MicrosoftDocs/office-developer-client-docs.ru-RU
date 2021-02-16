---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- Функция xloper12toxloper [excel 2007]
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

## <a name="parameters"></a>Параметры

_pxloper12_ (**LPXLOPER12)**
  
Указатель на исходный **XLOPER12 для** преобразования. 
  
_pxloper_ (**LPXLOPER)**
  
Указатель на целевой **объект XLOPER,** содержащий преобразованные значения. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

**TRUE,** если преобразование успешно, в противном случае **FALSE.** 
  
## <a name="remarks"></a>Примечания

В зависимости от типа **XLOPER12** эта функция выделяет новый буфер памяти для преобразованных значений, на которые указывают целевые **значения XLOPER.** Если преобразование успешно, вызываемая отвечает за освободить память, связанную с копией; **FreeXLOperT** можно использовать или сделать это напрямую с помощью **бесплатного .**
  
Если преобразование не удается, вызываемой не требуется освободить память.
  
Преобразование **из XLOPER12** в **XLOPER** может привести к сбою, если **XLOPER12** содержит слишком большой массив или ссылку или слишком длинную строку для **XLOPER.** 
  
**XLOPER12** Строки юникода с широкими символами преобразуются в строки byte **XLOPER** ASCII в зависимости от региональных стандартов. 
  
**XLOPER12** **xltypeInt** — это 32-битное подписанное integer, а **XLOPER** **xltypeInt** — 16-битное подписанное. Если предоставленное **integer XLOPER12** превышает ограничение, задаваемого в виде integer **XLOPER,** это количество преобразуется в 8-byte double и возвращается в **XLOPER** типа **xltypeNum.** Это единственный случай, в котором эта функция изменяет тип преобразованной **XLOPER.**
  
### <a name="example"></a>Пример

Код этой  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` функции см. в файле. 
  
## <a name="see-also"></a>См. также

- [Функции в библиотеке платформы](functions-in-the-framework-library.md)

