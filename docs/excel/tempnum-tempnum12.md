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
- функция tempnum12 [Excel 2007], функция TempNum [Excel 2007]
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
# <a name="tempnumtempnum12"></a><span data-ttu-id="9fd61-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="9fd61-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="9fd61-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9fd61-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9fd61-106">Функция библиотеки Framework, которая создает временную **XLOPER** /  **XLOPER12,** содержащую номер Microsoft Excel таблицы (двойной номер IEEE 8-byte).</span><span class="sxs-lookup"><span data-stu-id="9fd61-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="9fd61-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="9fd61-107">Parameters</span></span>

 <span data-ttu-id="9fd61-108">_d_ **(дважды)**</span><span class="sxs-lookup"><span data-stu-id="9fd61-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="9fd61-109">Предназначенное значение.</span><span class="sxs-lookup"><span data-stu-id="9fd61-109">The intended value.</span></span> <span data-ttu-id="9fd61-110">Обратите внимание, что подстанализные номера IEEE в настоящее время не поддерживаются и округляются до нуля.</span><span class="sxs-lookup"><span data-stu-id="9fd61-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="9fd61-111">Поддерживается отрицательная бесконечность.</span><span class="sxs-lookup"><span data-stu-id="9fd61-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="9fd61-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fd61-112">Return value</span></span>

<span data-ttu-id="9fd61-113">Возвращает числовую **xltypeNum,** содержащую значение, переданное в или ноль, если переданное значение было нестандартным.</span><span class="sxs-lookup"><span data-stu-id="9fd61-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9fd61-114">Пример</span><span class="sxs-lookup"><span data-stu-id="9fd61-114">Example</span></span>

<span data-ttu-id="9fd61-115">В этом примере используется **функция TempNum12,** чтобы передать аргумент **в xlfGetWorkspace.**</span><span class="sxs-lookup"><span data-stu-id="9fd61-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="9fd61-116">См. также</span><span class="sxs-lookup"><span data-stu-id="9fd61-116">See also</span></span>



[<span data-ttu-id="9fd61-117">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="9fd61-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

