---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- функция xlgethwnd [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807372"
---
# <a name="xlgethwnd"></a><span data-ttu-id="adca6-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="adca6-104">xlGetHwnd</span></span>

<span data-ttu-id="adca6-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="adca6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="adca6-106">Возвращает дескриптор окна верхнего уровня Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="adca6-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="adca6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="adca6-107">Parameters</span></span>

<span data-ttu-id="adca6-108">Эта функция не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="adca6-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="adca6-109">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adca6-109">Property value/Return value</span></span>

<span data-ttu-id="adca6-110">Содержит дескриптор окна (**xltypeInt**) в поле **val.w** .</span><span class="sxs-lookup"><span data-stu-id="adca6-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="adca6-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="adca6-111">Remarks</span></span>

<span data-ttu-id="adca6-112">Эта функция полезна для написания кода Windows API.</span><span class="sxs-lookup"><span data-stu-id="adca6-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="adca6-113">При вызове этой функции, с помощью [Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)переменной целое число возвращаемых XLOPER является подписанных короткий внутреннего 16-разрядный Это только может содержать низкой 16 бит дескриптор 32-разрядная версия Windows.</span><span class="sxs-lookup"><span data-stu-id="adca6-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="adca6-114">Чтобы найти высокой часть, код должен выполните итерацию по совпадение с низкой части всех открытых окон.</span><span class="sxs-lookup"><span data-stu-id="adca6-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="adca6-115">Начиная с версии Excel 2007, переменной integer **XLOPER12** является подписью int 32-разрядная версия и поэтому содержит весь дескриптор, нужно будет выполнять итерацию всех открытых окон.</span><span class="sxs-lookup"><span data-stu-id="adca6-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="adca6-116">Пример</span><span class="sxs-lookup"><span data-stu-id="adca6-116">Example</span></span>

<span data-ttu-id="adca6-117">Просмотр кода для [функции fShowDialog](fshowdialog.md) в `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="adca6-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="adca6-118">См. также</span><span class="sxs-lookup"><span data-stu-id="adca6-118">See also</span></span>

- [<span data-ttu-id="adca6-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="adca6-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="adca6-120">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="adca6-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

