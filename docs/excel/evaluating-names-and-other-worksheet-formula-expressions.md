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
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a><span data-ttu-id="4ea8a-104">Оценка имена и другие выражения формулы листа</span><span class="sxs-lookup"><span data-stu-id="4ea8a-104">Evaluating names and other worksheet formula expressions</span></span>

<span data-ttu-id="4ea8a-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4ea8a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4ea8a-106">Одной из наиболее важных функций, предоставляемых Excel через C API является возможность преобразования любой строки формулы, юридически должен быть введен в листе значение или массив значений.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-106">One of the most important features that Excel exposes through the C API is the ability to convert any string formula that can legally be entered into a worksheet to a value, or array of values.</span></span> <span data-ttu-id="4ea8a-107">Это важно для функции XLL и команды, которые должны прочитать содержимое определенные имена, например.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-107">This is essential for XLL functions and commands that must read the contents of defined names, for example.</span></span> <span data-ttu-id="4ea8a-108">Эта возможность предоставляется через [функцию xlfEvaluate](xlfevaluate.md), как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-108">This ability is exposed through the [xlfEvaluate function](xlfevaluate.md), as shown in this example.</span></span>
  
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

<span data-ttu-id="4ea8a-109">Обратите внимание на то, что при оценке имя листа, самостоятельно или в формуле, необходимо префикса имя с "!", по крайней мере.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-109">Note that when you are evaluating a worksheet name, either on its own or in a formula, you must prefix the name with '!', at least.</span></span> <span data-ttu-id="4ea8a-110">В противном случае Excel пытается найти имя в скрытых имен зарезервировано для библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-110">Otherwise, Excel tries to find the name in a hidden namespace reserved for DLLs.</span></span> <span data-ttu-id="4ea8a-111">Можно создавать и удалять скрытые имена библиотек DLL с помощью [функции xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="4ea8a-111">You can create and delete hidden DLL names using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="4ea8a-112">Можно получить определения любого определенное имя скрытого имя библиотеки DLL или имя листа, с помощью функции **xlfGetDef** .</span><span class="sxs-lookup"><span data-stu-id="4ea8a-112">You can get the definition of any defined name, whether it is a hidden DLL name or a worksheet name, using the **xlfGetDef** function.</span></span> 
  
<span data-ttu-id="4ea8a-113">Полная спецификация для имени листа принимает следующую форму:</span><span class="sxs-lookup"><span data-stu-id="4ea8a-113">The full specification for a worksheet name takes the following form:</span></span>
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
<span data-ttu-id="4ea8a-114">Обратите внимание, что Excel 2007 представлен ряд новых расширений файлов.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-114">Note that Excel 2007 introduced a number of new file extensions.</span></span> <span data-ttu-id="4ea8a-115">Можно опустить путь, имя книги и имя листа там, где имеется не неопределенность среди открытых книг в данном сеансе Excel.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-115">You can omit the path, the workbook name, and the sheet name where there is no ambiguity among the open workbooks in this Excel session.</span></span> 
  
<span data-ttu-id="4ea8a-116">В следующем примере оцениваются формулу `COUNT(A1:IV65536)` для активного листа и отображает результат.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-116">The next example evaluates the formula  `COUNT(A1:IV65536)` for the active worksheet and displays the result.</span></span> <span data-ttu-id="4ea8a-117">Обратите внимание на то необходимости в качестве префикса адреса диапазона с "!", который согласуется с соглашение диапазон ссылку на листах макросов XLM.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-117">Note the need to prefix the range address with '!', which is consistent with the range reference convention on XLM macro sheets.</span></span> <span data-ttu-id="4ea8a-118">Это соглашение о исходя из C API XLM:</span><span class="sxs-lookup"><span data-stu-id="4ea8a-118">The C API XLM follows this convention:</span></span> 
  
- <span data-ttu-id="4ea8a-119">`=A1`Ссылка на ячейку A1 на текущий лист макросов.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-119">`=A1` A reference to cell A1 on the current macro sheet.</span></span> <span data-ttu-id="4ea8a-120">(Не определен для XLL-модулей).</span><span class="sxs-lookup"><span data-stu-id="4ea8a-120">(Not defined for XLLs).</span></span> 
  
- <span data-ttu-id="4ea8a-121">`=!A1`Ссылка на ячейку A1 на активном листе (который может быть лист или лист макросов)</span><span class="sxs-lookup"><span data-stu-id="4ea8a-121">`=!A1` A reference to cell A1 on the active sheet (which could be a worksheet or macro sheet)</span></span> 
  
- <span data-ttu-id="4ea8a-122">`=Sheet1!A1`Ссылка на ячейку A1 на странице Лист1 в данном случае.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-122">`=Sheet1!A1` A reference to cell A1 on the specified sheet, Sheet1 in this case.</span></span> 
  
- <span data-ttu-id="4ea8a-123">`=[Book1.xls]Sheet1!A1`Ссылка на ячейку A1 на указанный лист в указанной книге.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-123">`=[Book1.xls]Sheet1!A1` A reference to cell A1 on the specified sheet in the specified workbook.</span></span> 
  
<span data-ttu-id="4ea8a-124">В надстройке XLL ссылку без начальных восклицательный (****!) не может преобразовать в значение.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-124">In an XLL, a reference without a leading exclamation point (**!**) cannot be converted to a value.</span></span> <span data-ttu-id="4ea8a-125">У него есть нет смысла, потому что нет нет активного листа макросов.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-125">It has no meaning because there is no current macro sheet.</span></span> <span data-ttu-id="4ea8a-126">Обратите внимание, что подкрепленное знак равенства (**=**) является необязательной и указан в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-126">Note that a leading equals sign (**=**) is optional and is omitted in the next example.</span></span>
  
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

<span data-ttu-id="4ea8a-127">Также можно использовать функцию **xlfEvaluate** для получения кода регистрации функции XLL из его зарегистрированное имя, которую можно использовать для вызова этой функции, с помощью [функции xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="4ea8a-127">You can also use the **xlfEvaluate** function to retrieve the registration ID of an XLL function from its registered name, which can then be used to call that function using the [xlUDF function](xludf.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="4ea8a-128">Зарегистрированное имя могут передаваться непосредственно в функцию **xlUDF** .</span><span class="sxs-lookup"><span data-stu-id="4ea8a-128">The registered name can be passed directly to the **xlUDF** function.</span></span> <span data-ttu-id="4ea8a-129">Это означает, что позволяет избежать необходимости оценка имя, чтобы получить идентификатор до вызова метода **xlUDF**.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-129">This means that you can avoid having to evaluate the name to get the ID before calling **xlUDF**.</span></span> <span data-ttu-id="4ea8a-130">Тем не менее если функция вызов количество раз, вызов его с помощью регистрации, идентификатор — быстрее.</span><span class="sxs-lookup"><span data-stu-id="4ea8a-130">However, if the function is to be called many times, calling it by using the registration ID is faster.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4ea8a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="4ea8a-131">See also</span></span>

- [<span data-ttu-id="4ea8a-132">Оценка выражений и листов Excel</span><span class="sxs-lookup"><span data-stu-id="4ea8a-132">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)
- [<span data-ttu-id="4ea8a-133">Разрешение прерывания длительных операций пользователем</span><span class="sxs-lookup"><span data-stu-id="4ea8a-133">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="4ea8a-134">Начало работы с пакетом SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="4ea8a-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

