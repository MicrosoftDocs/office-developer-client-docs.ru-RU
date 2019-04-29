---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- Функция xlfEvaluate [Excel 2007]
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
  
Использует средство синтаксического анализа Microsoft Excel и средство оценки функций для оценки любого выражения, которое можно ввести в ячейку листа.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Параметры

 _Пксформулатекст (Кслтипестр)_
  
Строка, которую необходимо оценить. Начальный знак равенства (=) является необязательным. Строка может быть любым текстом, который можно вводить в ячейку листа или листа макросов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает результат вычисления строки, которая может иметь тип **кслтипенум**, **кслтипестр**, **кслтипебул**, **кслтипирр**, **кслтипенил**, **xltypeMulti**.
  
## <a name="remarks"></a>Примечания

Строка может содержать только функции, а не эквиваленты команд. Это эквивалентно нажатию клавиши **F9** в строке формул. Если **xlfEvaluate** вызывается из функции листа XLL, зарегистрированной как потокобезопасным, выражение должно содержать только потокобезопасные функции. 
  
Основной способ использования функции **xlfEvaluate** заключается в том, чтобы разрешить DLL-библиотекам определить значение, присвоенное определенному имени, которое находится на листе или скрытом имени, определенном в библиотеке DLL. Обратите внимание на то, что в библиотеке DLL или XLL имя листа должно иметь префикс с восклицательным знаком (!), чтобы убедиться, что он интерпретируется как внешний для библиотеки DLL. Дополнительные сведения см в разделе [вычисленИе имен и других выражений в формулах листов](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **xlfEvaluate** не может использоваться для оценки ссылок на внешний лист, который не открыт. 
  
## <a name="example"></a>Пример

В этом примере используется **xlfEvaluate** для приведения текста "! B38 "к содержимому ячейки B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Эта функция вызывает макрос Command (**кслкалерт**) и правильно работает только при вызове из листа макросов или команды макроса.
  
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

