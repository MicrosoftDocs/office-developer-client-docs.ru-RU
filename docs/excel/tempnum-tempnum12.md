---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- Функция tempnum12 [excel 2007],TempNum function [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426634"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="d5e03-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="d5e03-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="d5e03-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d5e03-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d5e03-106">Функция библиотеки Framework, которая создает временную  /  **XLOPER XLOPER12,** содержащую номер листа Microsoft Excel (8-разрядный номер IEEE).</span><span class="sxs-lookup"><span data-stu-id="d5e03-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="d5e03-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5e03-107">Parameters</span></span>

 <span data-ttu-id="d5e03-108">_d_ (**double)**</span><span class="sxs-lookup"><span data-stu-id="d5e03-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="d5e03-109">Предполагаемая величина.</span><span class="sxs-lookup"><span data-stu-id="d5e03-109">The intended value.</span></span> <span data-ttu-id="d5e03-110">Обратите внимание, что в настоящее время не поддерживаются подстанстанты IEEE, которые округляются до нуля.</span><span class="sxs-lookup"><span data-stu-id="d5e03-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="d5e03-111">Поддерживается отрицательное бесконечность.</span><span class="sxs-lookup"><span data-stu-id="d5e03-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d5e03-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5e03-112">Return value</span></span>

<span data-ttu-id="d5e03-113">Возвращает число **xltypeNum,** содержащее значение, переданное в или ноль, если переданное значение было под нормали.</span><span class="sxs-lookup"><span data-stu-id="d5e03-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d5e03-114">Пример</span><span class="sxs-lookup"><span data-stu-id="d5e03-114">Example</span></span>

<span data-ttu-id="d5e03-115">В этом примере функция **TempNum12 используется** для передает аргумент **в xlfGetWorkspace.**</span><span class="sxs-lookup"><span data-stu-id="d5e03-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d5e03-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d5e03-116">See also</span></span>



[<span data-ttu-id="d5e03-117">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="d5e03-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

