---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- Функция xlCoerce [Excel 2007]
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
# <a name="xlcoerce"></a><span data-ttu-id="98ea3-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="98ea3-104">xlCoerce</span></span>

 <span data-ttu-id="98ea3-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="98ea3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="98ea3-106">Преобразует один **тип параметра**/ **XLOPER12** в другой или ищет значения ячеек на листе.</span><span class="sxs-lookup"><span data-stu-id="98ea3-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="98ea3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ea3-107">Parameters</span></span>

 <span data-ttu-id="98ea3-108">_пкссаурце_</span><span class="sxs-lookup"><span data-stu-id="98ea3-108">_pxSource_</span></span>
  
<span data-ttu-id="98ea3-109">**Исходная**/ **XLOPER12** , которую необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="98ea3-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="98ea3-110">_пксдесттипе_ (**кслтипеинт**)</span><span class="sxs-lookup"><span data-stu-id="98ea3-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="98ea3-111">(Необязательно).</span><span class="sxs-lookup"><span data-stu-id="98ea3-111">(Optional).</span></span> <span data-ttu-id="98ea3-112">Битовая маска получаемых типов, которые вы готовы принять.</span><span class="sxs-lookup"><span data-stu-id="98ea3-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="98ea3-113">Для указания нескольких возможных типов используйте оператор побитового **или** (|).</span><span class="sxs-lookup"><span data-stu-id="98ea3-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="98ea3-114">Если этот аргумент опущен, ссылки на отдельные ячейки преобразуются в один из типов значений **кслтипестр**, **кслтипенум**, **кслтипебул**, **кслтипирр**, **кслтипенил** (если ссылка на ячейку пуста), а ссылки на блоки ячеек преобразуются в **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="98ea3-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="98ea3-115">Это делает **xlCoerce** самым удобным способом поиска значений ячеек.</span><span class="sxs-lookup"><span data-stu-id="98ea3-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="98ea3-116">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98ea3-116">Property value/Return value</span></span>

<span data-ttu-id="98ea3-117">Возвращает приведенное значение (**кслтипестр**, **кслтипенум**, **кслтипебул**, **кслтипирр**, **кслтипенил**или **xltypeMulti**).</span><span class="sxs-lookup"><span data-stu-id="98ea3-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98ea3-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="98ea3-118">Remarks</span></span>

 <span data-ttu-id="98ea3-119">**xlCoerce** не удается выполнить преобразование в **кслтипебигдата** или **кслтипефлов**.</span><span class="sxs-lookup"><span data-stu-id="98ea3-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="98ea3-120">Передача типа **кслтипемиссинг** или **Кслтипенил** в качестве _пксдесттипе_ эквивалентна опущению аргумента.</span><span class="sxs-lookup"><span data-stu-id="98ea3-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="98ea3-121">В некоторых случаях может возникнуть ошибка преобразования.</span><span class="sxs-lookup"><span data-stu-id="98ea3-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="98ea3-122">Например, некоторые строки не могут быть преобразованы в числа, в то время как другие могут.</span><span class="sxs-lookup"><span data-stu-id="98ea3-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="98ea3-123">Если массив или ссылка на несколько ячеек преобразуются в один тип значения, результатом будет значение верхней левой ячейки или элемента массива.</span><span class="sxs-lookup"><span data-stu-id="98ea3-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="98ea3-124">Пример</span><span class="sxs-lookup"><span data-stu-id="98ea3-124">Example</span></span>

<span data-ttu-id="98ea3-125">Приведенный ниже код можно найти в `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="98ea3-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="98ea3-126">Функция **кслкалерт** неявно пытается преобразовать аргумент в строку, чтобы шаг приведения, показанный здесь, мог быть удален, а **ксинт** можно передать напрямую в **кслкалерт**.</span><span class="sxs-lookup"><span data-stu-id="98ea3-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="98ea3-127">Так как **кслкалерт** — командный макрос, этот код работает правильно только при вызове из листа макросов.</span><span class="sxs-lookup"><span data-stu-id="98ea3-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="98ea3-128">См. также</span><span class="sxs-lookup"><span data-stu-id="98ea3-128">See also</span></span>



[<span data-ttu-id="98ea3-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="98ea3-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="98ea3-130">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="98ea3-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

