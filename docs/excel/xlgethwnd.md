---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- xlgethwnd function [Excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425458"
---
# <a name="xlgethwnd"></a><span data-ttu-id="0ad6d-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="0ad6d-104">xlGetHwnd</span></span>

<span data-ttu-id="0ad6d-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0ad6d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0ad6d-106">Возвращает ручку окна верхнего Microsoft Excel окна.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="0ad6d-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0ad6d-107">Parameters</span></span>

<span data-ttu-id="0ad6d-108">Эта функция не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0ad6d-109">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ad6d-109">Property value/Return value</span></span>

<span data-ttu-id="0ad6d-110">Содержит ручку окна **(xltypeInt)** в **поле val.w.**</span><span class="sxs-lookup"><span data-stu-id="0ad6d-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0ad6d-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="0ad6d-111">Remarks</span></span>

<span data-ttu-id="0ad6d-112">Эта функция полезна для написания кода Windows API.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="0ad6d-113">При вызове этой функции с [помощью Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)возвращаемая переменная XLOPER является подписанной 16-битной короткой int. Это может содержать только 16-битную 32-Windows.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="0ad6d-114">Чтобы найти высокую часть, код должен итерировать через все открытые окна в поисках совпадения с низкой частью.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="0ad6d-115">Начиная с Excel 2007 г. целая переменная **XLOPER12** — это подписанный 32-битный int и, следовательно, содержит всю ручку, удаляя необходимость итерации всех открытых окон.</span><span class="sxs-lookup"><span data-stu-id="0ad6d-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="0ad6d-116">Пример</span><span class="sxs-lookup"><span data-stu-id="0ad6d-116">Example</span></span>

<span data-ttu-id="0ad6d-117">См. код функции [fShowDialog](fshowdialog.md)  `SAMPLES\GENERIC\GENERIC.C` в .</span><span class="sxs-lookup"><span data-stu-id="0ad6d-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ad6d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0ad6d-118">See also</span></span>

- [<span data-ttu-id="0ad6d-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="0ad6d-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="0ad6d-120">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="0ad6d-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

