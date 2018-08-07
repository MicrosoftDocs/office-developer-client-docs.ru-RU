---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- функция xlgetinst [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807359"
---
# <a name="xlgetinst"></a><span data-ttu-id="9c7a0-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="9c7a0-104">xlGetInst</span></span>

 <span data-ttu-id="9c7a0-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9c7a0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9c7a0-106">Возвращает экземпляр обработчика экземпляра Microsoft Excel, которые в настоящее время звонит библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="9c7a0-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="9c7a0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c7a0-107">Parameters</span></span>

<span data-ttu-id="9c7a0-108">Эта функция не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="9c7a0-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9c7a0-109">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c7a0-109">Property value/Return value</span></span>

<span data-ttu-id="9c7a0-110">В поле **val.w** будет дескриптор экземпляра (**xltypeInt**).</span><span class="sxs-lookup"><span data-stu-id="9c7a0-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9c7a0-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="9c7a0-111">Remarks</span></span>

<span data-ttu-id="9c7a0-112">Эта функция используется для различения нескольким экземплярам Excel, которые вызывают библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="9c7a0-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="9c7a0-113">При вызове этой функции, с помощью [Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)переменной целое число возвращаемых XLOPER является подписанных короткий внутреннего 16-разрядный Это только может содержать низкой 16 бит дескриптор 32-разрядная версия Windows.</span><span class="sxs-lookup"><span data-stu-id="9c7a0-113">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="9c7a0-114">Начиная с версии Excel 2007, переменной integer **XLOPER12** является подписью int 32-разрядная версия и поэтому содержит весь дескриптор, нужно будет выполнять итерацию всех открытых окон.</span><span class="sxs-lookup"><span data-stu-id="9c7a0-114">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9c7a0-115">Если функция **xlGetInst** используется в 64-разрядная версия Microsoft Excel, выберите функцию завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9c7a0-115">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail.</span></span> <span data-ttu-id="9c7a0-116">Это так, как тип значения **xltypeInt** ширины не хватает для хранения 64-разрядная версия длинный дескриптор, возвращенный Excel, в данном случае.</span><span class="sxs-lookup"><span data-stu-id="9c7a0-116">This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case.</span></span> <span data-ttu-id="9c7a0-117">Для этой цели Excel 2010 появились новые функции с именем [xlGetInstPtr](xlgetinstptr.md), который работает правильно с 32-разрядной и 64-разрядных версиях Excel.</span><span class="sxs-lookup"><span data-stu-id="9c7a0-117">For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9c7a0-118">Пример</span><span class="sxs-lookup"><span data-stu-id="9c7a0-118">Example</span></span>

<span data-ttu-id="9c7a0-119">В следующем примере сравниваются экземпляра последнюю копию Excel, которое вызывается для текущей копии Excel, который вызвал ее.</span><span class="sxs-lookup"><span data-stu-id="9c7a0-119">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="9c7a0-120">Если это так же, он возвращает 1; в противном случае возвращается значение 0; Если происходит сбой функции, возвращается значение -1.</span><span class="sxs-lookup"><span data-stu-id="9c7a0-120">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="9c7a0-121">См. также</span><span class="sxs-lookup"><span data-stu-id="9c7a0-121">See also</span></span>



[<span data-ttu-id="9c7a0-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="9c7a0-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="9c7a0-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="9c7a0-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="9c7a0-124">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="9c7a0-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

