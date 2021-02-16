---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- Функция xlstack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429981"
---
# <a name="xlstack"></a><span data-ttu-id="cb724-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="cb724-104">xlStack</span></span>

<span data-ttu-id="cb724-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cb724-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cb724-106">Проверяет объем пространства, оставленного в стеке.</span><span class="sxs-lookup"><span data-stu-id="cb724-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="cb724-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb724-107">Parameters</span></span>

<span data-ttu-id="cb724-108">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="cb724-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="cb724-109">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb724-109">Property value/Return value</span></span>

<span data-ttu-id="cb724-110">Возвращает количество оставшихся в стеке **(xltypeInt) bytes( xltypeInt).**</span><span class="sxs-lookup"><span data-stu-id="cb724-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb724-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="cb724-111">Remarks</span></span>

<span data-ttu-id="cb724-112">Объем доступного пространства стека последних версий переполнен 16-битным подписанным integer **XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="cb724-112">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**.</span></span> <span data-ttu-id="cb724-113">Это означает, что **xlStack** может возвращать значение между -32767 и 32768 при использовании **XLOPER** s и **Excel4** или **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="cb724-113">This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER** s and **Excel4** or **Excel4v**.</span></span> <span data-ttu-id="cb724-114">Чтобы получить правильное значение в этом случае, необходимо вернуть возвращенное значение к короткой без подписи.</span><span class="sxs-lookup"><span data-stu-id="cb724-114">To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="cb724-115">Начиная с Excel 2007, эту функцию следует вызывать с помощью **XLOPER12** и **Excel12** или **Excel12v.** В этом случае возвращаемой величиной является объем доступного пространства стека или 64 КБ, в зависимости от того, чем меньше.</span><span class="sxs-lookup"><span data-stu-id="cb724-115">Starting in Excel 2007, you should call this function using **XLOPER12** s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="cb724-116">Excel имеет ограниченный объем пространства в стеке, и не следует перегнастить это пространство.</span><span class="sxs-lookup"><span data-stu-id="cb724-116">Excel has a limited amount of space on the stack, and you should take care not to overrun this space.</span></span> <span data-ttu-id="cb724-117">Никогда не помещай в стек очень большие структуры данных и делайте как можно больше локальных переменных статическими.</span><span class="sxs-lookup"><span data-stu-id="cb724-117">Never put very large data structures on the stack, and make as many local variables as possible static.</span></span> <span data-ttu-id="cb724-118">Избегайте рекурсивного вызова функций, так как это быстро заполнит стек.</span><span class="sxs-lookup"><span data-stu-id="cb724-118">Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="cb724-119">Если вы подозреваете, что вы перезагруте стек, часто вызываем эту функцию, чтобы узнать, сколько места на стеке осталось.</span><span class="sxs-lookup"><span data-stu-id="cb724-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="cb724-120">Пример</span><span class="sxs-lookup"><span data-stu-id="cb724-120">Example</span></span>

<span data-ttu-id="cb724-121">В первом примере отображается оповещение, содержащее количество оставленного места в стеке и содержащееся в  `\SAMPLES\EXAMPLE\EXAMPLE.C` нем.</span><span class="sxs-lookup"><span data-stu-id="cb724-121">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="cb724-122">Второй пример делает то же самое, работая с **XLOPER** и не содержится в примере кода SDK.</span><span class="sxs-lookup"><span data-stu-id="cb724-122">The second example does the same thing, working with **XLOPER** s and is not contained in the SDK example code.</span></span>
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="cb724-123">См. также</span><span class="sxs-lookup"><span data-stu-id="cb724-123">See also</span></span>

- [<span data-ttu-id="cb724-124">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="cb724-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

