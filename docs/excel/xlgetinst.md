---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- Функция кслжетинст [Excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428132"
---
# <a name="xlgetinst"></a><span data-ttu-id="aa79c-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="aa79c-104">xlGetInst</span></span>

 <span data-ttu-id="aa79c-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="aa79c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="aa79c-106">Возвращает дескриптор экземпляра Microsoft Excel, который в данный момент вызывает библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="aa79c-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="aa79c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa79c-107">Parameters</span></span>

<span data-ttu-id="aa79c-108">У этой функции нет аргументов.</span><span class="sxs-lookup"><span data-stu-id="aa79c-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="aa79c-109">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa79c-109">Property value/Return value</span></span>

<span data-ttu-id="aa79c-110">Дескриптор экземпляра (**кслтипеинт**) будет указан в поле **Val. w** .</span><span class="sxs-lookup"><span data-stu-id="aa79c-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aa79c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa79c-111">Remarks</span></span>

<span data-ttu-id="aa79c-112">Эту функцию можно использовать для различения нескольких запущенных экземпляров Excel, вызывающих библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="aa79c-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="aa79c-113">При вызове этой функции с помощью [Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)возвращенная целочисленная переменная XLOPER имеет знак 16-bit short int. Это может быть только в том случае, если он содержит младшие 16 разрядов для дескриптора Windows 32-bit.</span><span class="sxs-lookup"><span data-stu-id="aa79c-113">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="aa79c-114">Начиная с версии Excel 2007, целочисленная переменная **XLOPER12** — это подписанное 32-разрядное целое число, поэтому он содержит весь дескриптор, устраняя необходимость в итерации всех открытых окон.</span><span class="sxs-lookup"><span data-stu-id="aa79c-114">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="aa79c-115">Если функция **кслжетинст** используется с 64-разрядной версией Microsoft Excel, функция завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="aa79c-115">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail.</span></span> <span data-ttu-id="aa79c-116">Это обусловлено тем, что тип значения **кслтипеинт** недостаточно широк для хранения 64-разрядных дескрипторов, возвращенных приложением Excel в данном случае.</span><span class="sxs-lookup"><span data-stu-id="aa79c-116">This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case.</span></span> <span data-ttu-id="aa79c-117">Для этой цели в Excel 2010 появилась новая функция с именем [кслжетинстптр](xlgetinstptr.md), которая правильно работает как с 32ом, так и с 64 – разрядной версией Excel.</span><span class="sxs-lookup"><span data-stu-id="aa79c-117">For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="aa79c-118">Пример</span><span class="sxs-lookup"><span data-stu-id="aa79c-118">Example</span></span>

<span data-ttu-id="aa79c-119">В следующем примере сравнивается экземпляр последней копии Excel, вызвавшей ее с текущей копией Excel.</span><span class="sxs-lookup"><span data-stu-id="aa79c-119">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="aa79c-120">Если они одинаковы, возвращается 1; в противном случае возвращается значение 0; Если функция завершается со сбоем, возвращается значение "– 1".</span><span class="sxs-lookup"><span data-stu-id="aa79c-120">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="aa79c-121">См. также</span><span class="sxs-lookup"><span data-stu-id="aa79c-121">See also</span></span>



[<span data-ttu-id="aa79c-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="aa79c-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="aa79c-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="aa79c-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="aa79c-124">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="aa79c-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

