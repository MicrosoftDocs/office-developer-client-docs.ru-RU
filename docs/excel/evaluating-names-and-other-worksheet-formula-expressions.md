---
title: Оценка имена и другие выражения формулы листа
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Вычисление выражения [excel 2007,] таблицы [Excel 2007] Имя оценки, оценка выражения [Excel 2007], оценка имена листов [Excel 2007], выражения [Excel 2007], оценки, оценка, имена [Excel 2007] Имя вычислений [Excel 2007] , преобразование значений, функция xlfEvaluate [Excel 2007], таблицы [Excel 2007], вычисление выражения строк [Excel 2007]
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9d726d89c859e2f7428b459971d5d13586f144e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807173"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Оценка имена и другие выражения формулы листа

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Одной из наиболее важных функций, предоставляемых Excel через C API является возможность преобразования любой строки формулы, юридически должен быть введен в листе значение или массив значений. Это важно для функции XLL и команды, которые должны прочитать содержимое определенные имена, например. Эта возможность предоставляется через [функцию xlfEvaluate](xlfevaluate.md), как показано в следующем примере.
  
```C
int WINAPI evaluate_name_example(void)
{
  wchar_t *expression = L"\016!MyDefinedName";
  XLOPER12 xNameText, xNameValue;
  xNameText.xltype = xltypeStr;
  xNameText.val.str = expression;
// Try to evaluate the name. Will fail with a #NAME? error
// if MyDefinedName is not defined in the active workbook.
  Excel12(xlfEvaluate, &xNameValue, 1, &xNameText);
// Attempt to convert the value to a string and display it in
// an alert dialog. This fails if xNameValue is an error value.
  Excel12(xlcAlert, 0, 1, &xNameValue);
// Must free xNameValue in case MyDefinedName evaluated to a string
  Excel12(xlFree, 0, 1, &xNameValue);
  return 1;
}
```

Обратите внимание на то, что при оценке имя листа, самостоятельно или в формуле, необходимо префикса имя с "!", по крайней мере. В противном случае Excel пытается найти имя в скрытых имен зарезервировано для библиотек DLL. Можно создавать и удалять скрытые имена библиотек DLL с помощью [функции xlfSetName](xlfsetname.md). Можно получить определения любого определенное имя скрытого имя библиотеки DLL или имя листа, с помощью функции **xlfGetDef** . 
  
Полная спецификация для имени листа принимает следующую форму:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Обратите внимание, что Excel 2007 представлен ряд новых расширений файлов. Можно опустить путь, имя книги и имя листа там, где имеется не неопределенность среди открытых книг в данном сеансе Excel. 
  
В следующем примере оцениваются формулу `COUNT(A1:IV65536)` для активного листа и отображает результат. Обратите внимание на то необходимости в качестве префикса адреса диапазона с "!", который согласуется с соглашение диапазон ссылку на листах макросов XLM. Это соглашение о исходя из C API XLM: 
  
- `=A1`Ссылка на ячейку A1 на текущий лист макросов. (Не определен для XLL-модулей). 
  
- `=!A1`Ссылка на ячейку A1 на активном листе (который может быть лист или лист макросов) 
  
- `=Sheet1!A1`Ссылка на ячейку A1 на странице Лист1 в данном случае. 
  
- `=[Book1.xls]Sheet1!A1`Ссылка на ячейку A1 на указанный лист в указанной книге. 
  
В надстройке XLL ссылку без начальных восклицательный (****!) не может преобразовать в значение. У него есть нет смысла, потому что нет нет активного листа макросов. Обратите внимание, что подкрепленное знак равенства (**=**) является необязательной и указан в следующем примере.
  
```C
int WINAPI evaluate_expression_example(void)
{
    wchar_t *expression = L"\022COUNT(!A1:IV65536)";
    XLOPER12 xExprText, xExprValue;
    xExprText.xltype = xltypeStr;
    xExprText.val.str = expression;
// Try to evaluate the formula.
    Excel12(xlfEvaluate, &xExprValue, 1, &xExprText);
// Attempt to convert the value to a string and display it in
// an alert dialog. Will fail if xExprValue is an error.
    Excel12(xlcAlert, 0, 1, &xExprValue);
// Not strictly necessary, as COUNT never returns a string
// but does no harm.
    Excel12(xlFree, 0, 1, &xExprValue);
    return 1;
}
```

Также можно использовать функцию **xlfEvaluate** для получения кода регистрации функции XLL из его зарегистрированное имя, которую можно использовать для вызова этой функции, с помощью [функции xlUDF](xludf.md).
  
> [!NOTE]
> Зарегистрированное имя могут передаваться непосредственно в функцию **xlUDF** . Это означает, что позволяет избежать необходимости оценка имя, чтобы получить идентификатор до вызова метода **xlUDF**. Тем не менее если функция вызов количество раз, вызов его с помощью регистрации, идентификатор — быстрее. 
  
## <a name="see-also"></a>См. также

- [Оценка выражений и листов Excel](excel-worksheet-and-expression-evaluation.md)
- [Разрешение прерывания длительных операций пользователем](permitting-user-breaks-in-lengthy-operations.md)
- [Начало работы с пакетом SDK XLL для Excel](getting-started-with-the-excel-xll-sdk.md)

