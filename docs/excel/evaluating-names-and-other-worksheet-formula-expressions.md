---
title: Оценка имен и других выражений в формулах листов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- оценка выражений [excel 2007],worksheets [Excel 2007], name evaluation,evaluating expressions [Excel 2007],evaluating worksheet names [Excel 2007],expressions [Excel 2007], evaluating,names [Excel 2007], evaluating,name evaluation [Excel 2007],strings [Excel 2007], converting to values,xlfEvaluate function [Excel 2007],worksheets [Excel 2007], expression evaluation
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
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a><span data-ttu-id="821a1-104">Оценка имен и других выражений в формулах листов</span><span class="sxs-lookup"><span data-stu-id="821a1-104">Evaluating names and other worksheet formula expressions</span></span>

<span data-ttu-id="821a1-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="821a1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="821a1-106">Одной из наиболее важных функций, которые Excel предоставляет через API C, является возможность преобразования строковых формул, которые могут быть введены на листах в значение или массив значений.</span><span class="sxs-lookup"><span data-stu-id="821a1-106">One of the most important features that Excel exposes through the C API is the ability to convert any string formula that can legally be entered into a worksheet to a value, or array of values.</span></span> <span data-ttu-id="821a1-107">Это необходимо, например, для функций и команд XLL, которые должны читать содержимое определенных имен.</span><span class="sxs-lookup"><span data-stu-id="821a1-107">This is essential for XLL functions and commands that must read the contents of defined names, for example.</span></span> <span data-ttu-id="821a1-108">Эта возможность отображается через функцию [xlfEvaluate,](xlfevaluate.md)как показано в этом примере.</span><span class="sxs-lookup"><span data-stu-id="821a1-108">This ability is exposed through the [xlfEvaluate function](xlfevaluate.md), as shown in this example.</span></span>
  
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

<span data-ttu-id="821a1-109">Обратите внимание, что при оценке имени таблицы (по формуле или по формуле) необходимо по крайней мере в качестве префикса к имени префикса "!".</span><span class="sxs-lookup"><span data-stu-id="821a1-109">Note that when you are evaluating a worksheet name, either on its own or in a formula, you must prefix the name with '!', at least.</span></span> <span data-ttu-id="821a1-110">В противном случае Excel пытается найти имя в скрытом пространстве имен, зарезервированном для DLL.</span><span class="sxs-lookup"><span data-stu-id="821a1-110">Otherwise, Excel tries to find the name in a hidden namespace reserved for DLLs.</span></span> <span data-ttu-id="821a1-111">Вы можете создавать и удалять скрытые имена DLL с помощью [функции xlfSetName.](xlfsetname.md)</span><span class="sxs-lookup"><span data-stu-id="821a1-111">You can create and delete hidden DLL names using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="821a1-112">С помощью функции **xlfGetDef** можно получить определение любого определенного имени( скрытого DLL-имени или имени таблицы).</span><span class="sxs-lookup"><span data-stu-id="821a1-112">You can get the definition of any defined name, whether it is a hidden DLL name or a worksheet name, using the **xlfGetDef** function.</span></span> 
  
<span data-ttu-id="821a1-113">Полная спецификация имени таблицы имеет следующую форму:</span><span class="sxs-lookup"><span data-stu-id="821a1-113">The full specification for a worksheet name takes the following form:</span></span>
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
<span data-ttu-id="821a1-114">Обратите внимание, что в Excel 2007 представлен ряд новых расширений файлов.</span><span class="sxs-lookup"><span data-stu-id="821a1-114">Note that Excel 2007 introduced a number of new file extensions.</span></span> <span data-ttu-id="821a1-115">Вы можете опустить путь, имя книги и имя листа, где нет неоднозначности между открытыми книгами в этом сеансе Excel.</span><span class="sxs-lookup"><span data-stu-id="821a1-115">You can omit the path, the workbook name, and the sheet name where there is no ambiguity among the open workbooks in this Excel session.</span></span> 
  
<span data-ttu-id="821a1-116">В следующем примере оценивается формула активного таблицы и отображается  `COUNT(A1:IV65536)` результат.</span><span class="sxs-lookup"><span data-stu-id="821a1-116">The next example evaluates the formula  `COUNT(A1:IV65536)` for the active worksheet and displays the result.</span></span> <span data-ttu-id="821a1-117">Обратите внимание на необходимость префикса адреса диапазона с префиксом "!", что согласуется с соглашением об обращениях к диапазону на листах макроса XLM.</span><span class="sxs-lookup"><span data-stu-id="821a1-117">Note the need to prefix the range address with '!', which is consistent with the range reference convention on XLM macro sheets.</span></span> <span data-ttu-id="821a1-118">XLM API C следует этому соглашению:</span><span class="sxs-lookup"><span data-stu-id="821a1-118">The C API XLM follows this convention:</span></span> 
  
- <span data-ttu-id="821a1-119">`=A1` Ссылка на ячейку A1 на текущем листе макроса.</span><span class="sxs-lookup"><span data-stu-id="821a1-119">`=A1` A reference to cell A1 on the current macro sheet.</span></span> <span data-ttu-id="821a1-120">(Не определено для XLL).</span><span class="sxs-lookup"><span data-stu-id="821a1-120">(Not defined for XLLs).</span></span> 
  
- <span data-ttu-id="821a1-121">`=!A1` Ссылка на ячейку A1 на активном листе (которая может быть листом или листом макроса)</span><span class="sxs-lookup"><span data-stu-id="821a1-121">`=!A1` A reference to cell A1 on the active sheet (which could be a worksheet or macro sheet)</span></span> 
  
- <span data-ttu-id="821a1-122">`=Sheet1!A1` Ссылка на ячейку A1 на указанном листе Sheet1 в данном случае.</span><span class="sxs-lookup"><span data-stu-id="821a1-122">`=Sheet1!A1` A reference to cell A1 on the specified sheet, Sheet1 in this case.</span></span> 
  
- <span data-ttu-id="821a1-123">`=[Book1.xls]Sheet1!A1` Ссылка на ячейку A1 на указанном листе в указанной книге.</span><span class="sxs-lookup"><span data-stu-id="821a1-123">`=[Book1.xls]Sheet1!A1` A reference to cell A1 on the specified sheet in the specified workbook.</span></span> 
  
<span data-ttu-id="821a1-124">В XLL ссылку без восклицания **(! !**) нельзя преобразовать в значение.</span><span class="sxs-lookup"><span data-stu-id="821a1-124">In an XLL, a reference without a leading exclamation point (**!**) cannot be converted to a value.</span></span> <span data-ttu-id="821a1-125">Это не имеет значения, так как нет текущего листа макроса.</span><span class="sxs-lookup"><span data-stu-id="821a1-125">It has no meaning because there is no current macro sheet.</span></span> <span data-ttu-id="821a1-126">Обратите внимание, что знак "равно" () является необязательным и опущен **=** в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="821a1-126">Note that a leading equals sign (**=**) is optional and is omitted in the next example.</span></span>
  
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

<span data-ttu-id="821a1-127">Вы также можете использовать функцию **xlfEvaluate,** чтобы получить ИД регистрации функции XLL из ее зарегистрированного имени, которое затем можно использовать для вызова этой функции с помощью функции [xlUDF.](xludf.md)</span><span class="sxs-lookup"><span data-stu-id="821a1-127">You can also use the **xlfEvaluate** function to retrieve the registration ID of an XLL function from its registered name, which can then be used to call that function using the [xlUDF function](xludf.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="821a1-128">Зарегистрированное имя можно передать непосредственно функции **xlUDF.**</span><span class="sxs-lookup"><span data-stu-id="821a1-128">The registered name can be passed directly to the **xlUDF** function.</span></span> <span data-ttu-id="821a1-129">Это означает, что вам не нужно будет оценивать имя, чтобы получить ИД, перед вызовом **xlUDF.**</span><span class="sxs-lookup"><span data-stu-id="821a1-129">This means that you can avoid having to evaluate the name to get the ID before calling **xlUDF**.</span></span> <span data-ttu-id="821a1-130">Однако если функция вызывается много раз, ее вызов с использованием ИД регистрации будет быстрее.</span><span class="sxs-lookup"><span data-stu-id="821a1-130">However, if the function is to be called many times, calling it by using the registration ID is faster.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="821a1-131">См. также</span><span class="sxs-lookup"><span data-stu-id="821a1-131">See also</span></span>

- [<span data-ttu-id="821a1-132">Оценка выражений и листов Excel</span><span class="sxs-lookup"><span data-stu-id="821a1-132">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)
- [<span data-ttu-id="821a1-133">Разрешение прерывания длительных операций пользователем</span><span class="sxs-lookup"><span data-stu-id="821a1-133">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="821a1-134">Начало работы с пакетом SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="821a1-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

