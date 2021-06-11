---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- функция tempactiverow [Excel 2007], функция TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413110"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="51fc7-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="51fc7-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="51fc7-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="51fc7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="51fc7-106">Функции библиотеки Framework, создав временную **XLOPER XLOPER12,** содержащую внешнюю ссылку на всю строку /   на активном листе.</span><span class="sxs-lookup"><span data-stu-id="51fc7-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="51fc7-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="51fc7-107">Parameters</span></span>

 <span data-ttu-id="51fc7-108">_строка_</span><span class="sxs-lookup"><span data-stu-id="51fc7-108">_row_</span></span>
  
<span data-ttu-id="51fc7-109">Строка, на который следует ссылаться.</span><span class="sxs-lookup"><span data-stu-id="51fc7-109">The row to be referenced.</span></span> <span data-ttu-id="51fc7-110">Аргументы строки основаны на нулевой основе, поэтому строка 1 передается в качестве 0.</span><span class="sxs-lookup"><span data-stu-id="51fc7-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="51fc7-111">В Microsoft Office Excel 2003 г. и более ранних версиях и начиная с Excel 2007 г. при запуске книги в режиме совместимости максимальное значение составляет 65 535 = 2^16 — 1 и является максимальным значением, которое может приниматься в integer WORD.</span><span class="sxs-lookup"><span data-stu-id="51fc7-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="51fc7-112">Начиная с Excel 2007 г. при запуске книги максимальное значение — 1 048 575 = 2^20 — 1.</span><span class="sxs-lookup"><span data-stu-id="51fc7-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="51fc7-113">RW определяется как 32-битный подписанный в XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="51fc7-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="51fc7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51fc7-114">Return value</span></span>

<span data-ttu-id="51fc7-115">Возвращает внешнюю **ссылку xltypeRef** на переданные ячейки строки.</span><span class="sxs-lookup"><span data-stu-id="51fc7-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="51fc7-116">Пример</span><span class="sxs-lookup"><span data-stu-id="51fc7-116">Example</span></span>

<span data-ttu-id="51fc7-117">В этом примере используется **функция TempActiveRow12** для выбора строки 113.</span><span class="sxs-lookup"><span data-stu-id="51fc7-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="51fc7-118">См. также</span><span class="sxs-lookup"><span data-stu-id="51fc7-118">See also</span></span>



[<span data-ttu-id="51fc7-119">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="51fc7-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

