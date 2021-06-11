---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- функция xlcoerce [Excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424835"
---
# <a name="xlcoerce"></a><span data-ttu-id="a0997-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="a0997-104">xlCoerce</span></span>

 <span data-ttu-id="a0997-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a0997-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a0997-106">Преобразует один тип **XLOPER** /  **XLOPER12 в** другой или ищет значения ячейки на листе.</span><span class="sxs-lookup"><span data-stu-id="a0997-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="a0997-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a0997-107">Parameters</span></span>

 <span data-ttu-id="a0997-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="a0997-108">_pxSource_</span></span>
  
<span data-ttu-id="a0997-109">Источник **XLOPER** /  **XLOPER12,** который необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="a0997-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="a0997-110">_pxDestType_ **(xltypeInt)**</span><span class="sxs-lookup"><span data-stu-id="a0997-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="a0997-111">(Необязательный).</span><span class="sxs-lookup"><span data-stu-id="a0997-111">(Optional).</span></span> <span data-ttu-id="a0997-112">Бит-маска из типов, которые вы готовы принять.</span><span class="sxs-lookup"><span data-stu-id="a0997-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="a0997-113">Для указания нескольких возможных типов следует использовать оператор **bitwise OR** (|).</span><span class="sxs-lookup"><span data-stu-id="a0997-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="a0997-114">Если этот аргумент опущен, ссылки на отдельные ячейки преобразуются в один из типов значений **xltypeStr,** **xltypeNum,** **xltypeBool,** **xltypeErr,** **xltypeNil** (если ссылаемая ячейка пуста), а ссылки на блоки клеток преобразуются в **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="a0997-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="a0997-115">Это делает **xlCoerce** наиболее удобным способом для наблюдения за значениями ячейки.</span><span class="sxs-lookup"><span data-stu-id="a0997-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a0997-116">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0997-116">Property value/Return value</span></span>

<span data-ttu-id="a0997-117">Возвращает принудительное значение **(xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, или **xltypeMulti**).</span><span class="sxs-lookup"><span data-stu-id="a0997-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0997-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0997-118">Remarks</span></span>

 <span data-ttu-id="a0997-119">**xlCoerce не может** преобразовать в **xltypeBigData** или **xltypeFlow.**</span><span class="sxs-lookup"><span data-stu-id="a0997-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="a0997-120">Передача **типа xltypeMissing** или **xltypeNil** в  _качестве pxDestType_ эквивалентна опущению аргумента.</span><span class="sxs-lookup"><span data-stu-id="a0997-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="a0997-121">В некоторых случаях преобразование может привести к сбойу.</span><span class="sxs-lookup"><span data-stu-id="a0997-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="a0997-122">Например, некоторые строки не могут быть преобразованы в числа, в то время как другие могут.</span><span class="sxs-lookup"><span data-stu-id="a0997-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="a0997-123">Если массив или многоклеточная ссылка преобразуется в один тип значения, результатом является значение верхнего левого элемента или элемента массива.</span><span class="sxs-lookup"><span data-stu-id="a0997-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="a0997-124">Пример</span><span class="sxs-lookup"><span data-stu-id="a0997-124">Example</span></span>

<span data-ttu-id="a0997-125">Следующий код можно найти в  `\SAMPLES\EXAMPLE\EXAMPLE.C` .</span><span class="sxs-lookup"><span data-stu-id="a0997-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a0997-126">Функция **xlcAlert** неявно пытается преобразовать аргумент в строку, чтобы показанный здесь шаг принуждения мог быть удален, а **xInt** можно передать непосредственно **в xlcAlert.**</span><span class="sxs-lookup"><span data-stu-id="a0997-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="a0997-127">Поскольку **xlcAlert** — это макрос команды, этот код работает правильно только при названии с макроса.</span><span class="sxs-lookup"><span data-stu-id="a0997-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a0997-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a0997-128">See also</span></span>



[<span data-ttu-id="a0997-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="a0997-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="a0997-130">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="a0997-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

