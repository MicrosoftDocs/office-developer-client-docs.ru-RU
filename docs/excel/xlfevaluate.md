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
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e468dc18b8f78f56acaa67c2f23dd53254088ad0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807347"
---
# <a name="xlfevaluate"></a><span data-ttu-id="baa0d-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="baa0d-104">xlfEvaluate</span></span>

 <span data-ttu-id="baa0d-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="baa0d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="baa0d-106">Метод средство синтаксического анализа Microsoft Excel и средство оценки функция для вычисления любое выражение, которое можно ввести в ячейку листа.</span><span class="sxs-lookup"><span data-stu-id="baa0d-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="baa0d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="baa0d-107">Parameters</span></span>

 <span data-ttu-id="baa0d-108">_pxFormulaText (xltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="baa0d-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="baa0d-109">Строка для оценки.</span><span class="sxs-lookup"><span data-stu-id="baa0d-109">The string to be evaluated.</span></span> <span data-ttu-id="baa0d-110">Ведущий знак равенства (=) не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="baa0d-110">A leading equal sign (=) is optional.</span></span> <span data-ttu-id="baa0d-111">Строка может быть любой текст, который юридическую можно вводить в ячейку листа электронной таблицы или макроса.</span><span class="sxs-lookup"><span data-stu-id="baa0d-111">The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="baa0d-112">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="baa0d-112">Property value/Return value</span></span>

<span data-ttu-id="baa0d-113">Возвращает результат вычисления строки, который может быть любой из типов **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="baa0d-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="baa0d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="baa0d-114">Remarks</span></span>

<span data-ttu-id="baa0d-115">Строка может содержать только функции, не эквивалентами команды.</span><span class="sxs-lookup"><span data-stu-id="baa0d-115">The string can contain only functions, not command equivalents.</span></span> <span data-ttu-id="baa0d-116">Это эквивалентно при нажатии клавиши **F9** в строке формул.</span><span class="sxs-lookup"><span data-stu-id="baa0d-116">It is equivalent to pressing **F9** from the formula bar.</span></span> <span data-ttu-id="baa0d-117">Если **xlfEvaluate** вызван из функции XLL листа, который был зарегистрирован как потокобезопасными, выражение должно содержать только функции являющихся потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="baa0d-117">If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="baa0d-118">Функция **xlfEvaluate** основном используется для разрешенных DLL-библиотеки значение, назначенное для определенного имени, либо на листе или скрытые имя, определенное в библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="baa0d-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL.</span></span> <span data-ttu-id="baa0d-119">Обратите внимание на то, что в DLL или XLL, имя листа должна начинаться с префикса по крайней мере восклицательный знак (!) чтобы убедиться, что он обрабатывается как внешними по отношению к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="baa0d-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="baa0d-120">Для получения дополнительных сведений см [Оценка имена и другие выражения формулы рабочего листа](evaluating-names-and-other-worksheet-formula-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="baa0d-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="baa0d-121">**xlfEvaluate** не может использоваться для оценки ссылки на внешние таблицы, которая не открыта.</span><span class="sxs-lookup"><span data-stu-id="baa0d-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="baa0d-122">Пример</span><span class="sxs-lookup"><span data-stu-id="baa0d-122">Example</span></span>

<span data-ttu-id="baa0d-123">В этом примере используется для присвоения текст **xlfEvaluate** «! B38» для содержимого ячейки B38.</span><span class="sxs-lookup"><span data-stu-id="baa0d-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="baa0d-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="baa0d-124"></span></span> <span data-ttu-id="baa0d-125">Эта функция вызывает команду макросов (**xlcAlert**) и будет работать только в том случае, когда вызывается из листа макросов или макроса.</span><span class="sxs-lookup"><span data-stu-id="baa0d-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="baa0d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="baa0d-126">See also</span></span>

- [<span data-ttu-id="baa0d-127">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="baa0d-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

