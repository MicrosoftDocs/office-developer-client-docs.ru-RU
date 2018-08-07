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
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807255"
---
# <a name="funcfib"></a><span data-ttu-id="2c76e-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="2c76e-104">FuncFib</span></span>

 <span data-ttu-id="2c76e-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2c76e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2c76e-106">Пример пользовательских функция, которая вычисляет n-й Фибоначчи.</span><span class="sxs-lookup"><span data-stu-id="2c76e-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="2c76e-107">При загрузке GENERIC.xll регистрирует эту функцию, чтобы его можно вызывать из рабочего листа.</span><span class="sxs-lookup"><span data-stu-id="2c76e-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="2c76e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c76e-108">Parameters</span></span>

 <span data-ttu-id="2c76e-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="2c76e-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="2c76e-110">Значение N, для которого необходим n-й Фибоначчи.</span><span class="sxs-lookup"><span data-stu-id="2c76e-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2c76e-111">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c76e-111">Property value/Return value</span></span>

<span data-ttu-id="2c76e-112">(**xltypeNum LPXLOPER12** в случае успешного выполнения или **xltypeErr** в противном случае —)</span><span class="sxs-lookup"><span data-stu-id="2c76e-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="2c76e-113">N-й Фибоначчи.</span><span class="sxs-lookup"><span data-stu-id="2c76e-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c76e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2c76e-114">Remarks</span></span>

<span data-ttu-id="2c76e-115">Функция использует определен в блоке функции как возвращаемое значение **XLOPER12**статическую переменную.</span><span class="sxs-lookup"><span data-stu-id="2c76e-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="2c76e-116">Это не потокобезопасными, и поэтому эта функция и любая другая функция, которая использует эту стратегию для возврата **XLOPER**или **XLOPER12**, не должны быть зарегистрированы как потокобезопасными, начиная с версии Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="2c76e-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="2c76e-117">Пример</span><span class="sxs-lookup"><span data-stu-id="2c76e-117">Example</span></span>

<span data-ttu-id="2c76e-118">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="2c76e-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c76e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2c76e-119">See also</span></span>



[<span data-ttu-id="2c76e-120">Функции из универсальной библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="2c76e-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

