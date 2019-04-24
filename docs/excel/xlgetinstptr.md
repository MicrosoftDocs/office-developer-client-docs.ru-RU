---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310054"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="8e4a8-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="8e4a8-103">xlGetInstPtr</span></span>

<span data-ttu-id="8e4a8-104">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8e4a8-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8e4a8-105">Возвращает дескриптор экземпляра Microsoft Excel, который в данный момент вызывает БИБЛИОТЕКУ DLL.</span><span class="sxs-lookup"><span data-stu-id="8e4a8-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="8e4a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e4a8-106">Parameters</span></span>

<span data-ttu-id="8e4a8-107">У этой функции нет аргументов.</span><span class="sxs-lookup"><span data-stu-id="8e4a8-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="8e4a8-108">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e4a8-108">Property value/Return value</span></span>

<span data-ttu-id="8e4a8-109">Дескриптор экземпляра (**кслтипебигдата**) будет указан в поле **Val. бигдата. h. хдата** .</span><span class="sxs-lookup"><span data-stu-id="8e4a8-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8e4a8-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="8e4a8-110">Remarks</span></span>

<span data-ttu-id="8e4a8-111">Эту функцию можно использовать для различения нескольких запущенных экземпляров Excel, вызывающих БИБЛИОТЕКУ DLL.</span><span class="sxs-lookup"><span data-stu-id="8e4a8-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="8e4a8-112">Эта функция возвращает правильное значение как с 32, так и с 64 – разрядной версией Excel.</span><span class="sxs-lookup"><span data-stu-id="8e4a8-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="8e4a8-113">Он появился в Excel 2010 как расширение функции [кслжетинст](xlgetinst.md) , которое правильно работает только с версиями Excel, поддерживающими только 32 бит.</span><span class="sxs-lookup"><span data-stu-id="8e4a8-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="8e4a8-114">Эта функция работает правильно при вызове с использованием [Excel4 и Excel12](excel4-excel12.md) с использованием функций обратного вызова API, так как обе структуры \*\*\*\* и структуры \*\*\*\* , поддерживающие значение **кслтипебигдата** Тип.</span><span class="sxs-lookup"><span data-stu-id="8e4a8-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8e4a8-115">Пример</span><span class="sxs-lookup"><span data-stu-id="8e4a8-115">Example</span></span>

<span data-ttu-id="8e4a8-116">В следующем примере сравнивается экземпляр последней копии Excel, вызвавшей ее с текущей копией Excel.</span><span class="sxs-lookup"><span data-stu-id="8e4a8-116">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="8e4a8-117">Если они одинаковы, возвращается 1; в противном случае возвращается значение 0; Если функция завершается со сбоем, возвращается значение "– 1".</span><span class="sxs-lookup"><span data-stu-id="8e4a8-117">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span> <span data-ttu-id="8e4a8-118">Этот пример работает как с 32, так и с 64 – разрядной версией Excel.</span><span class="sxs-lookup"><span data-stu-id="8e4a8-118">This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
    if (hNew != hOld)
    iRet = 0;
    else
    iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="8e4a8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8e4a8-119">See also</span></span>

- [<span data-ttu-id="8e4a8-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="8e4a8-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="8e4a8-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="8e4a8-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="8e4a8-122">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="8e4a8-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

