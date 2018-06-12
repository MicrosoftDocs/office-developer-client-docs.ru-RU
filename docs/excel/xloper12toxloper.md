---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- функция xloper12toxloper [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807370"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Процедура преобразования используются для преобразования из нового **XLOPER12** старый **XLOPER**.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parameters

_pxloper12_ (**LPXLOPER12**)
  
Указатель на источник **XLOPER12** преобразование. 
  
_pxloper_ (**LPXLOPER**)
  
Указатель на целевой **XLOPER** наличия преобразованное значение. 
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

**Значение TRUE,** Если преобразование выполнено успешно, **значение FALSE** в противном случае. 
  
## <a name="remarks"></a>Замечания

В зависимости от типа **XLOPER12**эта функция выделяет новый буфер памяти для преобразованные значения, которые являются направлена в целевом **XLOPER**. Вызывающий объект несет ответственность за освобождает память, связанных с копией ли преобразование будет успешно; Можно использовать **FreeXLOperT** или это можно сделать с помощью **свободного**.
  
В случае сбоя преобразования вызывающего освободить память, не требуется.
  
Преобразование из **XLOPER12** **XLOPER** может завершиться неудачно **XLOPER12** содержит массив или ссылку слишком большого размера или строка, слишком много времени для **XLOPER** для хранения. 
  
**XLOPER12** Строки двухбайтовых знаков Юникод преобразуются в строки байтов **XLOPER** ASCII в способом, зависящих от языковых стандартов. 
  
**XLOPER12** **xltypeInt** — 32-разрядное целое число со знаком, а **XLOPER** **xltypeInt** — 16-разрядное целое число со знаком. Когда предоставленное целое **XLOPER12** превышает ограничение **XLOPER** целого числа, целое число преобразуется в double 8 байтов и возвращаются в **XLOPER** из типа **xltypeNum**. Это единственный случай, в котором эта функция изменяет тип преобразованные **XLOPER**.
  
### <a name="example"></a>Пример

Просмотрите файл `\SAMPLES\FRAMEWRK\FRAMEWRK.C` код для этой функции. 
  
## <a name="see-also"></a>См. также

- [Функции в библиотеке Framework](functions-in-the-framework-library.md)

