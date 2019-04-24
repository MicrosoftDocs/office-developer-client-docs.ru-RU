---
title: Оценка имен и других выражений в формулах листов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Вычисление выражений [Excel 2007], листы [Excel 2007], вычисление имен, вычисление выражений [Excel 2007], Оценка имен листов [Excel 2007], выражения [Excel 2007], оценка, имена [Excel 2007], оценка, вычисление имен [Excel 2007] , строки [Excel 2007], преобразование в значения, функция xlfEvaluate [Excel 2007], листы [Excel 2007], вычисление выражений
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97328cbc57a9144a133524774e3be10a84a96bf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311118"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>Оценка имен и других выражений в формулах листов

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Одной из наиболее важных функций, предоставляемых приложением Excel через API C, является возможность преобразования любой строковой формулы, которая может быть введена на лист, в значение или массив значений. Это важно для функций XLL и команд, которые должны читать содержимое определенных имен, например. Эта возможность доступна через [функцию xlfEvaluate](xlfevaluate.md), как показано в этом примере.
  
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

Обратите внимание на то, что при оценке имени листа либо по его отношению к имени, либо в формуле необходимо по крайней мере префикс "!". В противном случае Excel пытается найти имя в скрытом пространстве имен, зарезервированном для библиотек DLL. Вы можете создавать и удалять скрытые имена DLL с помощью [функции xlfSetName](xlfsetname.md). Вы можете получить определение любого определенного имени, независимо от того, является ли оно скрытым именем DLL или именем листа с помощью функции **кслфжетдеф** . 
  
Полная спецификация имени листа имеет следующий вид:
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Обратите внимание, что в Excel 2007 появился ряд новых расширений файлов. Можно опустить путь, имя книги и имя листа, на котором нет неоднозначности между открытыми книгами в этом сеансе Excel. 
  
В следующем примере вычисляется формула `COUNT(A1:IV65536)` для активного листа и отображается результат. Обратите внимание, что необходимо добавить префикс адреса диапазона к параметру "!", который согласуется с соглашением о ссылочном диапазоне на листах макросов XLM. Для языка C API XLM следует следующее соглашение: 
  
- `=A1`Ссылка на ячейку a1 на текущем листе макроса. (Не определено для XLL-модулей). 
  
- `=!A1`Ссылка на ячейку a1 на активном листе (это может быть лист или лист макросов) 
  
- `=Sheet1!A1`Ссылка на ячейку a1 на указанном листе Sheet1 в данном случае. 
  
- `=[Book1.xls]Sheet1!A1`Ссылка на ячейку a1 на заданном листе указанной книги. 
  
В XLL-файле ссылка без начального восклицательного знака (**!**) не может быть преобразована в значение. Он не имеет смысла, так как отсутствует текущий лист макросов. Обратите внимание, что начальный знак**=** равенства () необязателен и не указывается в следующем примере.
  
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

Вы также можете использовать функцию **xlfEvaluate** для получения идентификатора регистрации функции XLL из зарегистрированного имени, которое затем можно использовать для вызова этой функции с помощью [функции xlUDF](xludf.md).
  
> [!NOTE]
> Зарегистрированное имя можно передать непосредственно в функцию **xlUDF** . Это означает, что вы можете избежать необходимости оценивать имя, чтобы получить идентификатор перед вызовом **xlUDF**. Тем не менее, если функция вызывается много раз, ее вызов с помощью идентификатора регистрации ускоряется. 
  
## <a name="see-also"></a>См. также

- [Оценка выражений и листов Excel](excel-worksheet-and-expression-evaluation.md)
- [Разрешение прерывания длительных операций пользователем](permitting-user-breaks-in-lengthy-operations.md)
- [Начало работы с пакетом SDK XLL для Excel](getting-started-with-the-excel-xll-sdk.md)

