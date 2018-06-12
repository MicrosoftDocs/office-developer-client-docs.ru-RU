---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- функция xlfevaluate [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e468dc18b8f78f56acaa67c2f23dd53254088ad0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807347"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Метод средство синтаксического анализа Microsoft Excel и средство оценки функция для вычисления любое выражение, которое можно ввести в ячейку листа.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Parameters

 _pxFormulaText (xltypeStr)_
  
Строка для оценки. Ведущий знак равенства (=) не является обязательным. Строка может быть любой текст, который юридическую можно вводить в ячейку листа электронной таблицы или макроса.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Возвращает результат вычисления строки, который может быть любой из типов **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.
  
## <a name="remarks"></a>Замечания

Строка может содержать только функции, не эквивалентами команды. Это эквивалентно при нажатии клавиши **F9** в строке формул. Если **xlfEvaluate** вызван из функции XLL листа, который был зарегистрирован как потокобезопасными, выражение должно содержать только функции являющихся потокобезопасными. 
  
Функция **xlfEvaluate** основном используется для разрешенных DLL-библиотеки значение, назначенное для определенного имени, либо на листе или скрытые имя, определенное в библиотеку DLL. Обратите внимание на то, что в DLL или XLL, имя листа должна начинаться с префикса по крайней мере восклицательный знак (!) чтобы убедиться, что он обрабатывается как внешними по отношению к библиотеке DLL. Для получения дополнительных сведений см [Оценка имена и другие выражения формулы рабочего листа](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **xlfEvaluate** не может использоваться для оценки ссылки на внешние таблицы, которая не открыта. 
  
## <a name="example"></a>Пример

В этом примере используется для присвоения текст **xlfEvaluate** «! B38» для содержимого ячейки B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Эта функция вызывает команду макросов (**xlcAlert**) и будет работать только в том случае, когда вызывается из листа макросов или макроса.
  
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

- [Функции API XLM важные и полезные C](essential-and-useful-c-api-xlm-functions.md)

