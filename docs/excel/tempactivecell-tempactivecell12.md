---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- Функция tempactivecell12 [excel 2007],Функция TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413194"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="49796-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="49796-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="49796-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="49796-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="49796-106">Функции библиотеки framework, которые создают временную **XLOPER12** /  **XLOPER12,** содержащую внешнюю ссылку на ячейку на активном листе.</span><span class="sxs-lookup"><span data-stu-id="49796-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="49796-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="49796-107">Parameters</span></span>

 <span data-ttu-id="49796-108">_row_</span><span class="sxs-lookup"><span data-stu-id="49796-108">_row_</span></span>
  
<span data-ttu-id="49796-109">Строка, на которая будет ссылаться.</span><span class="sxs-lookup"><span data-stu-id="49796-109">The row to be referenced.</span></span> <span data-ttu-id="49796-110">Аргументы строки основаны на нуле, поэтому строка 1 передается в качестве 0.</span><span class="sxs-lookup"><span data-stu-id="49796-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="49796-111">В Microsoft Office Excel 2003 и более ранних версий, а начиная с Excel 2007, в котором книга работает в режиме совместимости, максимальное значение составляет 65 535 = 2^16-1 и является максимальным значением, которое может приниматься в качестве значения, которое может приниматься в word integer.</span><span class="sxs-lookup"><span data-stu-id="49796-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="49796-112">Начиная с Excel 2007, где запущена книга, максимальное значение составляет 1 048 575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="49796-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="49796-113">RW определяется как 32-битное подписанное в XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="49796-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="49796-114">_col_</span><span class="sxs-lookup"><span data-stu-id="49796-114">_col_</span></span>
  
<span data-ttu-id="49796-115">Столбец, на который следует ссылаться.</span><span class="sxs-lookup"><span data-stu-id="49796-115">The column to be referenced.</span></span> <span data-ttu-id="49796-116">Это значение основано на нуле, поэтому столбец A передается как 0.</span><span class="sxs-lookup"><span data-stu-id="49796-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="49796-117">В Excel 2003 и более ранних версиях, а начиная с Excel 2007, где книга запущена в режиме совместимости, максимальное значение — 255 = 2^8- 1 и максимальное значение, которое может приниматься с помощью byTE-inte.</span><span class="sxs-lookup"><span data-stu-id="49796-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="49796-118">Начиная с Excel 2007, где запущена книга, максимальное значение — 16 383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="49796-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="49796-119">COL определяется как 32-битное подписанное в XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="49796-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="49796-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49796-120">Return value</span></span>

<span data-ttu-id="49796-121">Возвращает **внешнюю ссылку xltypeRef** на переданную ячейку.</span><span class="sxs-lookup"><span data-stu-id="49796-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="49796-122">Пример</span><span class="sxs-lookup"><span data-stu-id="49796-122">Example</span></span>

<span data-ttu-id="49796-123">В следующем примере **tempActiveCell12** используется для отображения содержимого B94 на активном листе.</span><span class="sxs-lookup"><span data-stu-id="49796-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="49796-124">См. также</span><span class="sxs-lookup"><span data-stu-id="49796-124">See also</span></span>



[<span data-ttu-id="49796-125">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="49796-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

