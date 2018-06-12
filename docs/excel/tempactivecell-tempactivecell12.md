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
- функция tempactivecell12 [excel 2007], функция TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807318"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="338c7-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="338c7-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="338c7-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="338c7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="338c7-106">Функции библиотеки Framework, создайте временный **XLOPER**/ **XLOPER12** , содержащий внешняя ссылка на ячейку на активном листе.</span><span class="sxs-lookup"><span data-stu-id="338c7-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="338c7-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="338c7-107">Parameters</span></span>

 <span data-ttu-id="338c7-108">_Строка_</span><span class="sxs-lookup"><span data-stu-id="338c7-108">_row_</span></span>
  
<span data-ttu-id="338c7-109">Ссылаться на строку.</span><span class="sxs-lookup"><span data-stu-id="338c7-109">The row to be referenced.</span></span> <span data-ttu-id="338c7-110">Строка аргументов с отсчетом от нуля, соответствующая строка 1 передается как 0.</span><span class="sxs-lookup"><span data-stu-id="338c7-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="338c7-111">В Microsoft Office Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 65 535 = 2 ^ 16-1, а — максимальное значение, которое может быть занято WORD integer.</span><span class="sxs-lookup"><span data-stu-id="338c7-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="338c7-112">Начиная с версии Excel 2007 под управлением книги, максимальное значение — 1 048 575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="338c7-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="338c7-113">RW определяется как 32-разрядное целое число со знаком в XLCALL. З.</span><span class="sxs-lookup"><span data-stu-id="338c7-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="338c7-114">_столбец_</span><span class="sxs-lookup"><span data-stu-id="338c7-114">_col_</span></span>
  
<span data-ttu-id="338c7-115">Ссылка на столбец.</span><span class="sxs-lookup"><span data-stu-id="338c7-115">The column to be referenced.</span></span> <span data-ttu-id="338c7-116">Это с отсчетом от нуля, поэтому этот столбец A передается как 0.</span><span class="sxs-lookup"><span data-stu-id="338c7-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="338c7-117">В Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 255 = 2 ^ 8-1, а — максимальное значение, которое может быть занято БАЙТОВОЕ целое число.</span><span class="sxs-lookup"><span data-stu-id="338c7-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="338c7-118">Начиная с версии Excel 2007 под управлением книги, максимальное значение — 16,383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="338c7-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="338c7-119">Столбец — это 32-разрядное целое число со знаком в XLCALL. З.</span><span class="sxs-lookup"><span data-stu-id="338c7-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="338c7-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="338c7-120">Return value</span></span>

<span data-ttu-id="338c7-121">Возвращает **xltypeRef** внешняя ссылка ячейки, переданные в.</span><span class="sxs-lookup"><span data-stu-id="338c7-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="338c7-122">Пример</span><span class="sxs-lookup"><span data-stu-id="338c7-122">Example</span></span>

<span data-ttu-id="338c7-123">В следующем примере используется **TempActiveCell12** для отображения содержимого B94 на активном листе.</span><span class="sxs-lookup"><span data-stu-id="338c7-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="338c7-124">См. также</span><span class="sxs-lookup"><span data-stu-id="338c7-124">See also</span></span>



[<span data-ttu-id="338c7-125">Функции в библиотеке Framework</span><span class="sxs-lookup"><span data-stu-id="338c7-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

