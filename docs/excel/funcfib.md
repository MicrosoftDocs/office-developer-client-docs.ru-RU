---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- функция funcfib [Excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423673"
---
# <a name="funcfib"></a><span data-ttu-id="250dd-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="250dd-104">FuncFib</span></span>

 <span data-ttu-id="250dd-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="250dd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="250dd-106">Пример функции таблицы, определяемой пользователем, которая вычисляет номер Nth Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="250dd-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="250dd-107">При загрузке GENERIC.xll она регистрирует эту функцию, чтобы она была вызвана из таблицы.</span><span class="sxs-lookup"><span data-stu-id="250dd-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="250dd-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="250dd-108">Parameters</span></span>

 <span data-ttu-id="250dd-109">_pxN_ **(LPXLOPER12)**</span><span class="sxs-lookup"><span data-stu-id="250dd-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="250dd-110">Значение N, для которого требуется номер Nth Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="250dd-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="250dd-111">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="250dd-111">Property value/Return value</span></span>

<span data-ttu-id="250dd-112">(**xltypeNum LPXLOPER12** при успешном или **xltypeErr** в противном случае)</span><span class="sxs-lookup"><span data-stu-id="250dd-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="250dd-113">Номер Nth Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="250dd-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="250dd-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="250dd-114">Remarks</span></span>

<span data-ttu-id="250dd-115">Функция использует статическую переменную, определяемую в блоке функций в качестве возвращаемой **величины XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="250dd-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="250dd-116">Это не безопасно, поэтому эта функция, и любая функция таблицы, использующая эту стратегию для возврата **XLOPER** s или **XLOPER12** s, не должна быть зарегистрирована в качестве безопасной для потока начиная с Excel 2007 г.</span><span class="sxs-lookup"><span data-stu-id="250dd-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER** s or **XLOPER12** s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="250dd-117">Пример</span><span class="sxs-lookup"><span data-stu-id="250dd-117">Example</span></span>

<span data-ttu-id="250dd-118">См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции.</span><span class="sxs-lookup"><span data-stu-id="250dd-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="250dd-119">См. также</span><span class="sxs-lookup"><span data-stu-id="250dd-119">See also</span></span>



[<span data-ttu-id="250dd-120">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="250dd-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

