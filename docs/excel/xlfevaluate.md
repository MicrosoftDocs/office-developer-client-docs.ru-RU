---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- функция xlfevaluate [Excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 527f7e932a41103c374e327a1bd0dd4c7d8e92a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439186"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Использует Microsoft Excel и оценщик функций для оценки любого выражения, которое может быть вписано в ячейку таблицы.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Parameters

 _pxFormulaText (xltypeStr)_
  
Строка, которая должна быть оценена. Ведущий равный знак (=) необязателен. Строка может быть любым текстом, который может быть юридически введен в лист или ячейку макроса.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает результат оценки строки, которая может быть любым из типов **xltypeNum,** **xltypeStr , xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**. 
  
## <a name="remarks"></a>Примечания

Строка может содержать только функции, а не эквиваленты команд. Это эквивалентно **нажатию F9 из** панели формулы. Если **xlfEvaluate** вызван из функции таблицы XLL, зарегистрированной в качестве безопасного потока, выражение должно содержать только функции, безопасные для потока. 
  
Основное использование функции **xlfEvaluate** — разрешить DLLs узнать значение, назначенное определенному имени, на листе или скрытое имя, определенное в DLL. Обратите внимание, что в DLL/XLL имя таблицы должно быть префиксом с по крайней мере восклицательный знак (!) для обеспечения того, чтобы оно интерпретируется как внешнее для DLL. Дополнительные сведения см. в списке "Оценка имен и других выражений [формулы таблицы".](evaluating-names-and-other-worksheet-formula-expressions.md)
  
 **xlfEvaluate** нельзя использовать для оценки ссылок на открытый внешний лист. 
  
## <a name="example"></a>Пример

В этом примере **xlfEvaluate** используется для принуждения текста "! B38" к содержимому ячейки B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Эта функция вызывает макрос команды **(xlcAlert)** и будет правильно работать только при вызове с макроса или в качестве команды макроса.
  
```cs
short WINAPI EvaluateExample(void)
{
    XLOPER12 xFormulaText, xRes, xRes2, xInt;
    xFormulaText.xltype = xltypeStr;
    xFormulaText.val.str = L"\004!B38";
    Excel12(xlfEvaluate, &xRes, 1, (LPXLOPER12)&xFormulaText);
    xInt.xltype = xltypeInt;
    xInt.val.w = 2;
    Excel12(xlcAlert, &xRes2, 2, (LPXLOPER12)&xRes, (LPXLOPER12)&xInt);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes2);
    return 1;
}
```

## <a name="see-also"></a>См. также

- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

