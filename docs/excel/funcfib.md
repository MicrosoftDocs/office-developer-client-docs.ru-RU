---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- Функция функфиб [Excel 2007]
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
# <a name="funcfib"></a><span data-ttu-id="00a1a-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="00a1a-104">FuncFib</span></span>

 <span data-ttu-id="00a1a-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00a1a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="00a1a-106">Пример пользовательской функции листа, которая вычисляет n число Фибоначчи.</span><span class="sxs-lookup"><span data-stu-id="00a1a-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="00a1a-107">Когда GENERIC. XLL загружается, она регистрирует эту функцию, чтобы ее можно было вызывать из листа.</span><span class="sxs-lookup"><span data-stu-id="00a1a-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="00a1a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="00a1a-108">Parameters</span></span>

 <span data-ttu-id="00a1a-109">_ПКСН_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="00a1a-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="00a1a-110">Значение N, для которого необходим n-й номер последовательности Фибоначчи.</span><span class="sxs-lookup"><span data-stu-id="00a1a-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="00a1a-111">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00a1a-111">Property value/Return value</span></span>

<span data-ttu-id="00a1a-112">(**КСЛТИПЕНУМ LPXLOPER12** в случае успеха или **кслтипирр** ).</span><span class="sxs-lookup"><span data-stu-id="00a1a-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="00a1a-113">Значение последовательности Фибоначчи (n).</span><span class="sxs-lookup"><span data-stu-id="00a1a-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00a1a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="00a1a-114">Remarks</span></span>

<span data-ttu-id="00a1a-115">В функции используется статическая переменная, определенная в блоке функции в качестве возвращаемого значения **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="00a1a-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="00a1a-116">Это не является потокобезопасным, поэтому эта функция и любая функция листа, использующая эту стратегию для возврата **XLOPER**s или **XLOPER12**, не должны регистрироваться как безопасный для потоков, начиная с Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="00a1a-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="00a1a-117">Пример</span><span class="sxs-lookup"><span data-stu-id="00a1a-117">Example</span></span>

<span data-ttu-id="00a1a-118">Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе.</span><span class="sxs-lookup"><span data-stu-id="00a1a-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00a1a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="00a1a-119">See also</span></span>



[<span data-ttu-id="00a1a-120">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="00a1a-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

