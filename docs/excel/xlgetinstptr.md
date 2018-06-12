---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807371"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="75332-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="75332-103">xlGetInstPtr</span></span>

<span data-ttu-id="75332-104">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="75332-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="75332-105">Возвращает экземпляр обработчика экземпляра Microsoft Excel, которые в настоящее время звонит библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="75332-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="75332-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="75332-106">Parameters</span></span>

<span data-ttu-id="75332-107">Эта функция не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="75332-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="75332-108">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75332-108">Property value/Return value</span></span>

<span data-ttu-id="75332-109">В поле **val.bigdata.h.hdata** будет дескриптор экземпляра (**xltypeBigData**).</span><span class="sxs-lookup"><span data-stu-id="75332-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="75332-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="75332-110">Remarks</span></span>

<span data-ttu-id="75332-111">Эта функция используется для различения нескольким экземплярам Excel, которые вызывают библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="75332-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="75332-112">Эта функция возвращает правильное значение с 32-разрядной и 64-разрядных версиях Excel.</span><span class="sxs-lookup"><span data-stu-id="75332-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="75332-113">Она была введена в Excel 2010 как расширение в функцию [xlGetInst](xlgetinst.md) , которая правильно работает только с 32-разрядных версиях Excel.</span><span class="sxs-lookup"><span data-stu-id="75332-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="75332-114">Эта функция работает правильно при вызове с помощью [Excel4 и Excel12](excel4-excel12.md) видов функции обратного вызова API, поскольку **XLOPER** и **XLOPER12** имеют ту же структуру, которая поддерживает значение **xltypeBigData** тип.</span><span class="sxs-lookup"><span data-stu-id="75332-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="75332-115">Пример</span><span class="sxs-lookup"><span data-stu-id="75332-115">Example</span></span>

<span data-ttu-id="75332-116">В следующем примере сравниваются экземпляра последнюю копию Excel, которое вызывается для текущей копии Excel, который вызвал ее.</span><span class="sxs-lookup"><span data-stu-id="75332-116">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="75332-117">Если это так же, он возвращает 1; в противном случае возвращается значение 0; Если происходит сбой функции, возвращается значение -1.</span><span class="sxs-lookup"><span data-stu-id="75332-117">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span> <span data-ttu-id="75332-118">В этом примере для работы с 32-разрядной и 64-разрядных версиях Excel.</span><span class="sxs-lookup"><span data-stu-id="75332-118">This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="75332-119">См. также</span><span class="sxs-lookup"><span data-stu-id="75332-119">See also</span></span>

- [<span data-ttu-id="75332-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="75332-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="75332-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="75332-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="75332-122">Функции интерфейса API для C, которые могут вызываться только из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="75332-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

