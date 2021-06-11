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
# <a name="xlfevaluate"></a><span data-ttu-id="9e6fc-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="9e6fc-104">xlfEvaluate</span></span>

 <span data-ttu-id="9e6fc-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9e6fc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9e6fc-106">Использует Microsoft Excel и оценщик функций для оценки любого выражения, которое может быть вписано в ячейку таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="9e6fc-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="9e6fc-107">Parameters</span></span>

 <span data-ttu-id="9e6fc-108">_pxFormulaText (xltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="9e6fc-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="9e6fc-109">Строка, которая должна быть оценена.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-109">The string to be evaluated.</span></span> <span data-ttu-id="9e6fc-110">Ведущий равный знак (=) необязателен.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-110">A leading equal sign (=) is optional.</span></span> <span data-ttu-id="9e6fc-111">Строка может быть любым текстом, который может быть юридически введен в лист или ячейку макроса.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-111">The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9e6fc-112">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e6fc-112">Property value/Return value</span></span>

<span data-ttu-id="9e6fc-113">Возвращает результат оценки строки, которая может быть любым из типов **xltypeNum,** **xltypeStr , xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**. </span><span class="sxs-lookup"><span data-stu-id="9e6fc-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e6fc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e6fc-114">Remarks</span></span>

<span data-ttu-id="9e6fc-115">Строка может содержать только функции, а не эквиваленты команд.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-115">The string can contain only functions, not command equivalents.</span></span> <span data-ttu-id="9e6fc-116">Это эквивалентно **нажатию F9 из** панели формулы.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-116">It is equivalent to pressing **F9** from the formula bar.</span></span> <span data-ttu-id="9e6fc-117">Если **xlfEvaluate** вызван из функции таблицы XLL, зарегистрированной в качестве безопасного потока, выражение должно содержать только функции, безопасные для потока.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-117">If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="9e6fc-118">Основное использование функции **xlfEvaluate** — разрешить DLLs узнать значение, назначенное определенному имени, на листе или скрытое имя, определенное в DLL.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL.</span></span> <span data-ttu-id="9e6fc-119">Обратите внимание, что в DLL/XLL имя таблицы должно быть префиксом с по крайней мере восклицательный знак (!) для обеспечения того, чтобы оно интерпретируется как внешнее для DLL.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="9e6fc-120">Дополнительные сведения см. в списке "Оценка имен и других выражений [формулы таблицы".](evaluating-names-and-other-worksheet-formula-expressions.md)</span><span class="sxs-lookup"><span data-stu-id="9e6fc-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="9e6fc-121">**xlfEvaluate** нельзя использовать для оценки ссылок на открытый внешний лист.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9e6fc-122">Пример</span><span class="sxs-lookup"><span data-stu-id="9e6fc-122">Example</span></span>

<span data-ttu-id="9e6fc-123">В этом примере **xlfEvaluate** используется для принуждения текста "! B38" к содержимому ячейки B38.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="9e6fc-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="9e6fc-125">Эта функция вызывает макрос команды **(xlcAlert)** и будет правильно работать только при вызове с макроса или в качестве команды макроса.</span><span class="sxs-lookup"><span data-stu-id="9e6fc-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="9e6fc-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9e6fc-126">See also</span></span>

- [<span data-ttu-id="9e6fc-127">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="9e6fc-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

