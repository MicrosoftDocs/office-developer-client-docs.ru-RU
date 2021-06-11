---
title: Оценка имен и других выражений в формулах листов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- оценка выражений [Excel 2007], таблицы [Excel 2007], оценка имен, оценка выражений [Excel 2007], оценка имен листа [Excel 2007], выражения [Excel 2007], evaluationing,names [Excel 2007], assessmenting,name assessment [Excel 2007], strings [Excel 2007], converting to values,xlfEvaluate function [Excel 2007],worksheets [Excel 2007], expression assessment
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97328cbc57a9144a133524774e3be10a84a96bf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406866"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Оценка имен и других выражений в формулах листов

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Одной из наиболее важных функций Excel которая предоставляется через API C, является возможность преобразования любой строки формулы, которую можно юридически вставить в таблицу в значение или массив значений. Это необходимо для функций и команд XLL, которые должны читать содержимое определенных имен, например. Эта способность подвергается воздействию функции [xlfEvaluate,](xlfevaluate.md)как показано в этом примере.
  
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

Обратите внимание, что при оценке имени таблицы как самостоятельно, так и по формуле необходимо как минимум префиксить имя с помощью "!". В противном Excel пытается найти имя в скрытом пространстве имен, зарезервированном для DLLs. Вы можете создавать и удалять скрытые имена DLL с помощью [функции xlfSetName.](xlfsetname.md) Вы можете получить определение любого определенного имени, будь то скрытое имя DLL или имя таблицы, используя **функцию xlfGetDef.** 
  
Полная спецификация для имени таблицы принимает следующую форму:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Обратите внимание, Excel 2007 г. был представлен ряд новых расширений файлов. Вы можете опустить путь, имя книги и имя листа, где нет двусмысленности среди открытых книг в этом Excel сессии. 
  
В следующем примере оценивается формула для активного таблицы  `COUNT(A1:IV65536)` и отображается результат. Обратите внимание на необходимость префикса адреса диапазона с помощью "!", соответствующего конвенции о диапазоне ссылок на макрос XLM. XLM C API следует этой конвенции: 
  
- `=A1` Ссылка на ячейку A1 на текущем листе макроса. (Не определено для XLLs). 
  
- `=!A1` Ссылка на ячейку A1 на активном листе (которая может быть листом или макрос) 
  
- `=Sheet1!A1` Ссылка на ячейку A1 на указанном листе, sheet1 в этом случае. 
  
- `=[Book1.xls]Sheet1!A1` Ссылка на ячейку A1 на указанном листе в указанной книге. 
  
В XLL ссылка без ведущего восклицания **(! )** не может быть преобразована в значение. Это не имеет значения, так как нет текущего макроса. Обратите внимание, что ведущий знак равного () необязателен и **=** опущен в следующем примере.
  
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

Вы также можете использовать функцию **xlfEvaluate** для получения регистрационного ID функции XLL из зарегистрированного имени, которое затем можно использовать для вызова этой функции с помощью [функции xlUDF](xludf.md).
  
> [!NOTE]
> Зарегистрированное имя можно передать непосредственно функции **xlUDF.** Это означает, что вы можете избежать необходимости оценивать имя, чтобы получить ID перед вызовом **xlUDF**. Однако если функцию нужно вызывать много раз, вызывать ее с помощью регистрационного ИД можно быстрее. 
  
## <a name="see-also"></a>См. также

- [Оценка выражений и листов Excel](excel-worksheet-and-expression-evaluation.md)
- [Разрешение прерывания длительных операций пользователем](permitting-user-breaks-in-lengthy-operations.md)
- [Начало работы с пакетом SDK XLL для Excel](getting-started-with-the-excel-xll-sdk.md)

