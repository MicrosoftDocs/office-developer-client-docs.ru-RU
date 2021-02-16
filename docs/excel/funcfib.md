---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- функция funcfib [excel 2007]
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
# <a name="funcfib"></a><span data-ttu-id="a72b6-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="a72b6-104">FuncFib</span></span>

 <span data-ttu-id="a72b6-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a72b6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a72b6-106">Пример определяемой пользователем функции таблицы, которая вычисляет Nth Fibonacci number.</span><span class="sxs-lookup"><span data-stu-id="a72b6-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="a72b6-107">При загрузке GENERIC.xll она регистрирует эту функцию, чтобы ее можно было вызвано с помощью таблицы.</span><span class="sxs-lookup"><span data-stu-id="a72b6-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="a72b6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a72b6-108">Parameters</span></span>

 <span data-ttu-id="a72b6-109">_pxN_ (**LPXLOPER12)**</span><span class="sxs-lookup"><span data-stu-id="a72b6-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="a72b6-110">Значение N, для которого требуется N-й номер Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="a72b6-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a72b6-111">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a72b6-111">Property value/Return value</span></span>

<span data-ttu-id="a72b6-112">(**xltypeNum LPXLOPER12,** если успешно или **xltypeErr в противном случае)**</span><span class="sxs-lookup"><span data-stu-id="a72b6-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="a72b6-113">N-й номер Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="a72b6-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a72b6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a72b6-114">Remarks</span></span>

<span data-ttu-id="a72b6-115">Функция использует статическую переменную, определяемую в блоке функции, в качестве возвращаемой **переменной XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="a72b6-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="a72b6-116">Это не потокобезопасная функция, поэтому эта функция и любая функция листа, использующая эту стратегию для возврата S или **XLOPER12 XLOPER12,** не должна быть зарегистрирована как потокобезопасная, начиная с Excel 2007. </span><span class="sxs-lookup"><span data-stu-id="a72b6-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER** s or **XLOPER12** s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="a72b6-117">Пример</span><span class="sxs-lookup"><span data-stu-id="a72b6-117">Example</span></span>

<span data-ttu-id="a72b6-118">См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="a72b6-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a72b6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a72b6-119">See also</span></span>



[<span data-ttu-id="a72b6-120">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="a72b6-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

