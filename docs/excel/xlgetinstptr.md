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
# <a name="xlgetinstptr"></a><span data-ttu-id="d3f3f-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="d3f3f-103">xlGetInstPtr</span></span>

<span data-ttu-id="d3f3f-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d3f3f-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d3f3f-105">Возвращает handle экземпляра Microsoft Excel, который в настоящее время вызывает DLL.</span><span class="sxs-lookup"><span data-stu-id="d3f3f-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="d3f3f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3f3f-106">Parameters</span></span>

<span data-ttu-id="d3f3f-107">Эта функция не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="d3f3f-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d3f3f-108">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3f3f-108">Property value/Return value</span></span>

<span data-ttu-id="d3f3f-109">Handle экземпляра (**xltypeBigData)** будет в **поле val.bigdata.h.hdata.**</span><span class="sxs-lookup"><span data-stu-id="d3f3f-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d3f3f-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3f3f-110">Remarks</span></span>

<span data-ttu-id="d3f3f-111">Эту функцию можно использовать для различия между несколькими запущенными экземплярами Excel, которые вызывает DLL.</span><span class="sxs-lookup"><span data-stu-id="d3f3f-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="d3f3f-112">Эта функция возвращает правильное значение для 32- и 64-битных версий Excel.</span><span class="sxs-lookup"><span data-stu-id="d3f3f-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="d3f3f-113">Она была представлена в Excel 2010 как расширение функции [xlGetInst,](xlgetinst.md) которая правильно работает только с 32-битными версиями Excel.</span><span class="sxs-lookup"><span data-stu-id="d3f3f-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="d3f3f-114">Эта функция работает правильно при вызове с помощью вариантов Функции вызова API Excel4 и [Excel12,](excel4-excel12.md) так как **XLOPER** и **XLOPER12** имеют ту же структуру, которая поддерживает тип значения **xltypeBigData.**</span><span class="sxs-lookup"><span data-stu-id="d3f3f-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d3f3f-115">Пример</span><span class="sxs-lookup"><span data-stu-id="d3f3f-115">Example</span></span>

<span data-ttu-id="d3f3f-116">В следующем примере сравнивается экземпляр последней копии Excel, которая вызвала его, с текущей копией Excel, которая ее вызвала.</span><span class="sxs-lookup"><span data-stu-id="d3f3f-116">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="d3f3f-117">Если они одинаковы, возвращается 1; Если нет, возвращается 0; если функция не работает, она возвращает -1.</span><span class="sxs-lookup"><span data-stu-id="d3f3f-117">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span> <span data-ttu-id="d3f3f-118">Этот пример работает как с 32-, так и с 64-битными версиями Excel.</span><span class="sxs-lookup"><span data-stu-id="d3f3f-118">This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="d3f3f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d3f3f-119">See also</span></span>

- [<span data-ttu-id="d3f3f-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="d3f3f-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="d3f3f-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="d3f3f-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="d3f3f-122">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="d3f3f-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

