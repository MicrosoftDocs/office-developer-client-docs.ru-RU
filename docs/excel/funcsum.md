---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- функция funcsum [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 0b991cf5cdae90522abc9512193ee556e4c6e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807263"
---
# <a name="funcsum"></a><span data-ttu-id="b1eb4-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="b1eb4-104">FuncSum</span></span>

 <span data-ttu-id="b1eb4-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b1eb4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b1eb4-106">Пример пользовательских функция, которая принимает аргументы усечение и вычисляет их сумма.</span><span class="sxs-lookup"><span data-stu-id="b1eb4-106">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum.</span></span> <span data-ttu-id="b1eb4-107">Каждый аргумент может быть единые номера, диапазон или массив.</span><span class="sxs-lookup"><span data-stu-id="b1eb4-107">Each argument can be a single number, a range, or an array.</span></span> <span data-ttu-id="b1eb4-108">При загрузке GENERIC.xll регистрирует эту функцию, чтобы его можно вызывать из рабочего листа.</span><span class="sxs-lookup"><span data-stu-id="b1eb4-108">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="b1eb4-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="b1eb4-109">Parameters</span></span>

 <span data-ttu-id="b1eb4-110">_px1 px29_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="b1eb4-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="b1eb4-111">Указатели на **XLOPER12** аргументов.</span><span class="sxs-lookup"><span data-stu-id="b1eb4-111">Pointers to **XLOPER12** arguments.</span></span> <span data-ttu-id="b1eb4-112">Функция принимает любой тип ввода, но закодированные только для работы с номера, литерал массивы номера и диапазоны, содержащие только числа или пустые ячейки.</span><span class="sxs-lookup"><span data-stu-id="b1eb4-112">The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells.</span></span> <span data-ttu-id="b1eb4-113">Если не указано меньше 29 аргументов, оставшихся аргументов как **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="b1eb4-113">If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b1eb4-114">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1eb4-114">Property value/Return value</span></span>

<span data-ttu-id="b1eb4-115">(**LPXLOPER12 xltypeNum** или **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="b1eb4-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="b1eb4-116">Суммы аргументы или #VALUE!</span><span class="sxs-lookup"><span data-stu-id="b1eb4-116">The sum of the arguments or #VALUE!</span></span> <span data-ttu-id="b1eb4-117">При наличии других символов, в списке заданный аргумент или в ячейку в диапазоне или элемент массива.</span><span class="sxs-lookup"><span data-stu-id="b1eb4-117">if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="b1eb4-118">Пример</span><span class="sxs-lookup"><span data-stu-id="b1eb4-118">Example</span></span>

<span data-ttu-id="b1eb4-119">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="b1eb4-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1eb4-120">См. также</span><span class="sxs-lookup"><span data-stu-id="b1eb4-120">See also</span></span>



[<span data-ttu-id="b1eb4-121">В универсальные библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="b1eb4-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

