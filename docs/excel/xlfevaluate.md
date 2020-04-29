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
# <a name="xlfevaluate"></a><span data-ttu-id="ecf82-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="ecf82-104">xlfEvaluate</span></span>

 <span data-ttu-id="ecf82-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ecf82-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ecf82-106">Использует средство синтаксического анализа Microsoft Excel и средство оценки функций для оценки любого выражения, которое можно ввести в ячейку листа.</span><span class="sxs-lookup"><span data-stu-id="ecf82-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="ecf82-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecf82-107">Parameters</span></span>

 <span data-ttu-id="ecf82-108">_Пксформулатекст (Кслтипестр)_</span><span class="sxs-lookup"><span data-stu-id="ecf82-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="ecf82-109">Строка, которую необходимо оценить.</span><span class="sxs-lookup"><span data-stu-id="ecf82-109">The string to be evaluated.</span></span> <span data-ttu-id="ecf82-110">Начальный знак равенства (=) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ecf82-110">A leading equal sign (=) is optional.</span></span> <span data-ttu-id="ecf82-111">Строка может быть любым текстом, который можно вводить в ячейку листа или листа макросов.</span><span class="sxs-lookup"><span data-stu-id="ecf82-111">The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ecf82-112">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecf82-112">Property value/Return value</span></span>

<span data-ttu-id="ecf82-113">Возвращает результат вычисления строки, которая может иметь тип **кслтипенум**, **кслтипестр**, **кслтипебул**, **кслтипирр**, **кслтипенил**, **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="ecf82-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ecf82-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ecf82-114">Remarks</span></span>

<span data-ttu-id="ecf82-115">Строка может содержать только функции, а не эквиваленты команд.</span><span class="sxs-lookup"><span data-stu-id="ecf82-115">The string can contain only functions, not command equivalents.</span></span> <span data-ttu-id="ecf82-116">Это эквивалентно нажатию клавиши **F9** в строке формул.</span><span class="sxs-lookup"><span data-stu-id="ecf82-116">It is equivalent to pressing **F9** from the formula bar.</span></span> <span data-ttu-id="ecf82-117">Если **xlfEvaluate** вызывается из функции листа XLL, зарегистрированной как потокобезопасным, выражение должно содержать только потокобезопасные функции.</span><span class="sxs-lookup"><span data-stu-id="ecf82-117">If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="ecf82-118">Основной способ использования функции **xlfEvaluate** заключается в том, чтобы разрешить DLL-библиотекам определить значение, присвоенное определенному имени, которое находится на листе или скрытом имени, определенном в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="ecf82-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL.</span></span> <span data-ttu-id="ecf82-119">Обратите внимание на то, что в библиотеке DLL или XLL имя листа должно иметь префикс с восклицательным знаком (!), чтобы убедиться, что он интерпретируется как внешний для библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="ecf82-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="ecf82-120">Дополнительные сведения см в разделе [Вычисление имен и других выражений в формулах листов](evaluating-names-and-other-worksheet-formula-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="ecf82-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="ecf82-121">**xlfEvaluate** не может использоваться для оценки ссылок на внешний лист, который не открыт.</span><span class="sxs-lookup"><span data-stu-id="ecf82-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ecf82-122">Пример</span><span class="sxs-lookup"><span data-stu-id="ecf82-122">Example</span></span>

<span data-ttu-id="ecf82-123">В этом примере используется **xlfEvaluate** для приведения текста "! B38 "к содержимому ячейки B38.</span><span class="sxs-lookup"><span data-stu-id="ecf82-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="ecf82-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="ecf82-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="ecf82-125">Эта функция вызывает макрос Command (**кслкалерт**) и правильно работает только при вызове из листа макросов или команды макроса.</span><span class="sxs-lookup"><span data-stu-id="ecf82-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="ecf82-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ecf82-126">See also</span></span>

- [<span data-ttu-id="ecf82-127">Необходимые и полезные функции XLM из API C</span><span class="sxs-lookup"><span data-stu-id="ecf82-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

