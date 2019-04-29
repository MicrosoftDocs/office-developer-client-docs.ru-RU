---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- Функция tempint12 [Excel 2007], функция Темпинт [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 16a2222dbc51ad9480dbd5941ca2ed13f65b55e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438752"
---
# <a name="tempinttempint12"></a><span data-ttu-id="c0927-104">TempInt/TempInt12</span><span class="sxs-lookup"><span data-stu-id="c0927-104">TempInt/TempInt12</span></span>

 <span data-ttu-id="c0927-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c0927-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c0927-106">Функция библиотеки Framework, которая создает временную структуру **XLOPER**/ \*\*\*\* , содержащую целое число.</span><span class="sxs-lookup"><span data-stu-id="c0927-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** that contains an integer.</span></span> 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a><span data-ttu-id="c0927-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0927-107">Parameters</span></span>

 <span data-ttu-id="c0927-108">_i_</span><span class="sxs-lookup"><span data-stu-id="c0927-108">_i_</span></span>
  
<span data-ttu-id="c0927-109">Предполагаемое целое значение.</span><span class="sxs-lookup"><span data-stu-id="c0927-109">The intended integer value.</span></span> <span data-ttu-id="c0927-110">Обратите внимание, что значение **XLOPER** — это 16-разрядное целое число со знаком (short int), а значение **XLOPER12** — это 32-разрядное целое число ([Long] int).</span><span class="sxs-lookup"><span data-stu-id="c0927-110">Note that the **XLOPER** integer is a signed 16-bit integer (short int), whereas the **XLOPER12** integer is a signed 32-bit integer ([long] int).</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="c0927-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0927-111">Return value</span></span>

<span data-ttu-id="c0927-112">Возвращает целое число **кслтипеинт** , содержащее переданное значение.</span><span class="sxs-lookup"><span data-stu-id="c0927-112">Returns an **xltypeInt** integer containing the value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c0927-113">Пример</span><span class="sxs-lookup"><span data-stu-id="c0927-113">Example</span></span>

<span data-ttu-id="c0927-114">В этом примере функция **TempInt12** используется для передачи аргумента в **кслфжетворкспаце**.</span><span class="sxs-lookup"><span data-stu-id="c0927-114">This example uses the **TempInt12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c0927-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c0927-115">See also</span></span>



[<span data-ttu-id="c0927-116">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="c0927-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

