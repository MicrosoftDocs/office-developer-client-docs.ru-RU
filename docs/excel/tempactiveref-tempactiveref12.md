---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- Функция tempactiveref [excel 2007],Функция TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415546"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="d3d4f-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="d3d4f-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="d3d4f-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d3d4f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d3d4f-106">Функция библиотеки Framework, которая создает временную  /  **XLOPER XLOPER12,** содержащую внешнюю ссылку на прямоугольный блок ячеек на активном листе.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="d3d4f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3d4f-107">Parameters</span></span>

 <span data-ttu-id="d3d4f-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="d3d4f-108">_rwFirst_</span></span>
  
<span data-ttu-id="d3d4f-109">Начальная строка ссылки.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="d3d4f-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="d3d4f-110">_rwLast_</span></span>
  
<span data-ttu-id="d3d4f-111">Конечная строка ссылки.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="d3d4f-112">Аргументы строки основаны на нуле, поэтому строка 1 передается в качестве 0.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-112">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="d3d4f-113">В Microsoft Office Excel 2003 и более ранних версий, а начиная с Excel 2007, где книга работает в режиме совместимости, максимальное значение составляет 65 535 = 2^16–1 и является максимальным значением, которое может приниматься в word integer.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-113">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="d3d4f-114">Начиная с Excel 2007, где запущена книга, максимальное значение — 1 048 575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-114">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="d3d4f-115">RW определяется как 32-битное подписанное в XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-115">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="d3d4f-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="d3d4f-116">_colFirst_</span></span>
  
<span data-ttu-id="d3d4f-117">Номер начального столбца ссылки.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="d3d4f-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="d3d4f-118">_colLast_</span></span>
  
<span data-ttu-id="d3d4f-119">Номер конечного столбца ссылки.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="d3d4f-120">Аргументы столбцов основаны на нуле, поэтому столбец A передается в качестве 0.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-120">Column arguments are zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="d3d4f-121">В Excel 2003 и более ранних версиях, а начиная с Excel 2007, где книга запущена в режиме совместимости, максимальное значение — 255 = 2^8- 1 и максимальное значение, которое может приниматься с помощью byTE-inte.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-121">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="d3d4f-122">Начиная с Excel 2007, где запущена книга, максимальное значение — 16 383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-122">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="d3d4f-123">COL определяется как 32-битное подписанное в XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-123">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d3d4f-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3d4f-124">Return value</span></span>

<span data-ttu-id="d3d4f-125">Возвращает **внешнюю ссылку xltypeRef** на прямоугольный блок переданных ячеек.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d3d4f-126">Пример</span><span class="sxs-lookup"><span data-stu-id="d3d4f-126">Example</span></span>

<span data-ttu-id="d3d4f-127">В этом примере функция **TempActiveRef12** используется для выбора ячеек A105:C110.</span><span class="sxs-lookup"><span data-stu-id="d3d4f-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d3d4f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d3d4f-128">See also</span></span>



[<span data-ttu-id="d3d4f-129">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="d3d4f-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

