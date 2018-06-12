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
- функция tempint12 [excel 2007], функция TempInt [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807329"
---
# <a name="tempinttempint12"></a><span data-ttu-id="8098e-104">TempInt/TempInt12</span><span class="sxs-lookup"><span data-stu-id="8098e-104">TempInt/TempInt12</span></span>

 <span data-ttu-id="8098e-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8098e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8098e-106">Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** , содержащее целое число.</span><span class="sxs-lookup"><span data-stu-id="8098e-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** that contains an integer.</span></span> 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a><span data-ttu-id="8098e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8098e-107">Parameters</span></span>

 <span data-ttu-id="8098e-108">_я_</span><span class="sxs-lookup"><span data-stu-id="8098e-108">_i_</span></span>
  
<span data-ttu-id="8098e-109">Предполагаемая целое значение.</span><span class="sxs-lookup"><span data-stu-id="8098e-109">The intended integer value.</span></span> <span data-ttu-id="8098e-110">Обратите внимание, что целое число **XLOPER** 16-разрядного целого числа со знаком (короткий int), тогда как **XLOPER12** целое число — 32-разрядная версия целого числа со знаком (int [длинный]).</span><span class="sxs-lookup"><span data-stu-id="8098e-110">Note that the **XLOPER** integer is a signed 16-bit integer (short int), whereas the **XLOPER12** integer is a signed 32-bit integer ([long] int).</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="8098e-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="8098e-111">Return value</span></span>

<span data-ttu-id="8098e-112">Возвращает **xltypeInt** целое значение, переданное в.</span><span class="sxs-lookup"><span data-stu-id="8098e-112">Returns an **xltypeInt** integer containing the value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8098e-113">Пример</span><span class="sxs-lookup"><span data-stu-id="8098e-113">Example</span></span>

<span data-ttu-id="8098e-114">В этом примере используется функция **TempInt12** для передачи аргумента **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="8098e-114">This example uses the **TempInt12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="8098e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8098e-115">See also</span></span>



[<span data-ttu-id="8098e-116">Функции в библиотеке Framework</span><span class="sxs-lookup"><span data-stu-id="8098e-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

