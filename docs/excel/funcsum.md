---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- функция funcsum [Excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406943"
---
# <a name="funcsum"></a><span data-ttu-id="471e9-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="471e9-104">FuncSum</span></span>

 <span data-ttu-id="471e9-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="471e9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="471e9-106">Пример функции таблицы, определяемой пользователем, которая принимает от 1 до 29 аргументов и вычисляет их сумму.</span><span class="sxs-lookup"><span data-stu-id="471e9-106">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum.</span></span> <span data-ttu-id="471e9-107">Каждый аргумент может быть одним числом, диапазоном или массивом.</span><span class="sxs-lookup"><span data-stu-id="471e9-107">Each argument can be a single number, a range, or an array.</span></span> <span data-ttu-id="471e9-108">При загрузке GENERIC.xll она регистрирует эту функцию, чтобы она была вызвана из таблицы.</span><span class="sxs-lookup"><span data-stu-id="471e9-108">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="471e9-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="471e9-109">Parameters</span></span>

 <span data-ttu-id="471e9-110">_px1-px29_ **(LPXLOPER12)**</span><span class="sxs-lookup"><span data-stu-id="471e9-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="471e9-111">Указатели на **аргументы XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="471e9-111">Pointers to **XLOPER12** arguments.</span></span> <span data-ttu-id="471e9-112">Функция принимает любой тип ввода, но кодируется только для работы с числами, литеральными массивами чисел и диапазонами, содержащими только цифры или пустые ячейки.</span><span class="sxs-lookup"><span data-stu-id="471e9-112">The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells.</span></span> <span data-ttu-id="471e9-113">Если предоставлено менее 29 аргументов, остальные аргументы будут предоставлены в **качестве xltypeMissing.**</span><span class="sxs-lookup"><span data-stu-id="471e9-113">If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="471e9-114">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="471e9-114">Property value/Return value</span></span>

<span data-ttu-id="471e9-115">(**LPXLOPER12 xltypeNum** или **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="471e9-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="471e9-116">Сумма аргументов или #VALUE!</span><span class="sxs-lookup"><span data-stu-id="471e9-116">The sum of the arguments or #VALUE!</span></span> <span data-ttu-id="471e9-117">если в списке предоставленных аргументов нет числовых данных или в ячейке в диапазоне или элементе массива.</span><span class="sxs-lookup"><span data-stu-id="471e9-117">if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="471e9-118">Пример</span><span class="sxs-lookup"><span data-stu-id="471e9-118">Example</span></span>

<span data-ttu-id="471e9-119">См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции.</span><span class="sxs-lookup"><span data-stu-id="471e9-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="471e9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="471e9-120">See also</span></span>



[<span data-ttu-id="471e9-121">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="471e9-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

