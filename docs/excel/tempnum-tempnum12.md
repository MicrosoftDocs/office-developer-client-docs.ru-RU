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
- функция tempnum12 [excel 2007], функция TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807326"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="b8c61-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="b8c61-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="b8c61-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b8c61-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b8c61-106">Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** , содержащее число лист Microsoft Excel (IEEE double 8 байтов).</span><span class="sxs-lookup"><span data-stu-id="b8c61-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="b8c61-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8c61-107">Parameters</span></span>

 <span data-ttu-id="b8c61-108">_d_ (**double**)</span><span class="sxs-lookup"><span data-stu-id="b8c61-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="b8c61-109">Целевое значение.</span><span class="sxs-lookup"><span data-stu-id="b8c61-109">The intended value.</span></span> <span data-ttu-id="b8c61-110">Обратите внимание, что IEEE вложенных обычных чисел в настоящее время не поддерживается округляются до нуля.</span><span class="sxs-lookup"><span data-stu-id="b8c61-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="b8c61-111">Отрицательное infinity поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b8c61-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b8c61-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="b8c61-113">Возвращает числовое **xltypeNum** , содержащая значение переданного или ноль, если переданное значение было вложенных обычный.</span><span class="sxs-lookup"><span data-stu-id="b8c61-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b8c61-114">Пример</span><span class="sxs-lookup"><span data-stu-id="b8c61-114">Example</span></span>

<span data-ttu-id="b8c61-115">В этом примере используется функция **TempNum12** для передачи аргумента **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="b8c61-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="b8c61-116">См. также</span><span class="sxs-lookup"><span data-stu-id="b8c61-116">See also</span></span>



[<span data-ttu-id="b8c61-117">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="b8c61-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

