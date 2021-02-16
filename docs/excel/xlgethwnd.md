---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- Функция xlgethwnd [excel 2007]
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
# <a name="xlgethwnd"></a><span data-ttu-id="c9c33-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="c9c33-104">xlGetHwnd</span></span>

<span data-ttu-id="c9c33-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c9c33-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c9c33-106">Возвращает окне окне верхнего уровня Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c9c33-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="c9c33-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9c33-107">Parameters</span></span>

<span data-ttu-id="c9c33-108">Эта функция не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="c9c33-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c9c33-109">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9c33-109">Property value/Return value</span></span>

<span data-ttu-id="c9c33-110">Содержит окне **(xltypeInt)** в **поле val.w.**</span><span class="sxs-lookup"><span data-stu-id="c9c33-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c9c33-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9c33-111">Remarks</span></span>

<span data-ttu-id="c9c33-112">Эта функция полезна для написания кода API Windows.</span><span class="sxs-lookup"><span data-stu-id="c9c33-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="c9c33-113">При вызове этой функции с помощью [Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)возвращаемая переменная XLOPER является подписанной 16-битной короткой переменной. Это может содержать только 16-битные 32-битные 32-битные точки Windows.</span><span class="sxs-lookup"><span data-stu-id="c9c33-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="c9c33-114">Чтобы найти высокую часть, код должен проходить по всем открытым окнам в поисках совпадения с низкой частью.</span><span class="sxs-lookup"><span data-stu-id="c9c33-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="c9c33-115">Начиная с Excel 2007, целомерная переменная **XLOPER12** — это 32-битное целое значение, которое содержит весь лад, удаляя необходимость в итерации всех открытых окон.</span><span class="sxs-lookup"><span data-stu-id="c9c33-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="c9c33-116">Пример</span><span class="sxs-lookup"><span data-stu-id="c9c33-116">Example</span></span>

<span data-ttu-id="c9c33-117">См. код функции [fShowDialog](fshowdialog.md) в  `SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="c9c33-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9c33-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c9c33-118">See also</span></span>

- [<span data-ttu-id="c9c33-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="c9c33-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="c9c33-120">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="c9c33-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

