---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405284"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="f797b-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="f797b-103">xlGetInstPtr</span></span>

<span data-ttu-id="f797b-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f797b-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f797b-105">Возвращает ручку экземпляра экземпляра Microsoft Excel, который в настоящее время вызывает DLL.</span><span class="sxs-lookup"><span data-stu-id="f797b-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="f797b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f797b-106">Parameters</span></span>

<span data-ttu-id="f797b-107">Эта функция не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="f797b-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f797b-108">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f797b-108">Property value/Return value</span></span>

<span data-ttu-id="f797b-109">Ручка экземпляра **(xltypeBigData)** будет в **поле val.bigdata.h.hdata.**</span><span class="sxs-lookup"><span data-stu-id="f797b-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f797b-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="f797b-110">Remarks</span></span>

<span data-ttu-id="f797b-111">Эта функция может использоваться для различия между несколькими запущенными экземплярами Excel, вызываемой DLL.</span><span class="sxs-lookup"><span data-stu-id="f797b-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="f797b-112">Эта функция возвращает правильное значение с 32-битными и 64-битными версиями Excel.</span><span class="sxs-lookup"><span data-stu-id="f797b-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="f797b-113">Она была представлена Excel 2010 г. в качестве расширения функции [xlGetInst,](xlgetinst.md) которая работает правильно только с 32-битными версиями Excel.</span><span class="sxs-lookup"><span data-stu-id="f797b-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="f797b-114">Эта функция работает правильно, если она вызвана с помощью вариантов Excel4 и [Excel12](excel4-excel12.md) функций вызова API, так как оба **XLOPER** и **XLOPER12** имеют ту же структуру, которая поддерживает тип **значения xltypeBigData.**</span><span class="sxs-lookup"><span data-stu-id="f797b-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f797b-115">Пример</span><span class="sxs-lookup"><span data-stu-id="f797b-115">Example</span></span>

<span data-ttu-id="f797b-116">В следующем примере сравнивает экземпляр последней копии Excel, назвавшей его текущей копией Excel, назвавшей его.</span><span class="sxs-lookup"><span data-stu-id="f797b-116">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="f797b-117">Если они одинаковы, возвращается 1; если нет, он возвращает 0; если функция не работает, она возвращает -1.</span><span class="sxs-lookup"><span data-stu-id="f797b-117">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span> <span data-ttu-id="f797b-118">Этот пример работает с 32-битными и 64-битными версиями Excel.</span><span class="sxs-lookup"><span data-stu-id="f797b-118">This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="f797b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f797b-119">See also</span></span>

- [<span data-ttu-id="f797b-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="f797b-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="f797b-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="f797b-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="f797b-122">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="f797b-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

