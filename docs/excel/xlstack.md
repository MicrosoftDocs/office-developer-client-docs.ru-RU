---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- функция xlstack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807367"
---
# <a name="xlstack"></a><span data-ttu-id="dcb5e-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="dcb5e-104">xlStack</span></span>

<span data-ttu-id="dcb5e-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="dcb5e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="dcb5e-106">Проверка свободного места в стеке.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="dcb5e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcb5e-107">Parameters</span></span>

<span data-ttu-id="dcb5e-108">Эта функция не получает никаких аргументов.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="dcb5e-109">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcb5e-109">Property value/Return value</span></span>

<span data-ttu-id="dcb5e-110">Возвращает число байт (**xltypeInt**), оставшихся в стеке.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dcb5e-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="dcb5e-111">Remarks</span></span>

<span data-ttu-id="dcb5e-112">Объем доступных стек последних версий выходящее за 16-разрядного целого числа со знаком из **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-112">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**.</span></span> <span data-ttu-id="dcb5e-113">Это означает, что этот **xlStack** может возвращать значение между-32767 и 32768 при вызове с помощью **XLOPER**s и **Excel4** или **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-113">This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER**s and **Excel4** or **Excel4v**.</span></span> <span data-ttu-id="dcb5e-114">Чтобы получить правильное значение в этом случае, необходимо привести возвращаемое значение для неподписанных short.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-114">To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="dcb5e-115">Начиная с версии Excel 2007, необходимо вызвать эту функцию, с помощью **XLOPER12**s и **Excel12** или **Excel12v**, является случай возвращаемое значение, свободное место стека или 64 КБ, какое из значений является меньшим.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-115">Starting in Excel 2007, you should call this function using **XLOPER12**s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="dcb5e-116">Excel имеет ограниченный объем пространства в стеке, после чего следует позаботиться не к переполнению этого пространства.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-116">Excel has a limited amount of space on the stack, and you should take care not to overrun this space.</span></span> <span data-ttu-id="dcb5e-117">Никогда не создавать очень больших структур данных в стеке и сделать статические столько локальных переменных по мере возможности.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-117">Never put very large data structures on the stack, and make as many local variables as possible static.</span></span> <span data-ttu-id="dcb5e-118">Избегайте функции рекурсивный вызов, так как, который будет быстро заполняется стека.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-118">Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="dcb5e-119">Если предполагается, что переполнение стека, эта функция часто, чтобы увидеть, сколько места стека.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="dcb5e-120">Пример</span><span class="sxs-lookup"><span data-stu-id="dcb5e-120">Example</span></span>

<span data-ttu-id="dcb5e-121">В первом примере отображаются сообщения с оповещением, содержащий объем места для стека и содержащихся в `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-121">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="dcb5e-122">Во втором примере выполняются те же действия, работа с **XLOPER**s и не находится в примере кода пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-122">The second example does the same thing, working with **XLOPER**s and is not contained in the SDK example code.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="dcb5e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="dcb5e-123">See also</span></span>

- [<span data-ttu-id="dcb5e-124">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="dcb5e-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

