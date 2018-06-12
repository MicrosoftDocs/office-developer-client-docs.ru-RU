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
- функция tempactiveref [excel 2007], функция TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807321"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="88c76-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="88c76-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="88c76-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="88c76-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="88c76-106">Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** , содержащий внешняя ссылка прямоугольный блок ячеек на активном листе.</span><span class="sxs-lookup"><span data-stu-id="88c76-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="88c76-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="88c76-107">Parameters</span></span>

 <span data-ttu-id="88c76-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="88c76-108">_rwFirst_</span></span>
  
<span data-ttu-id="88c76-109">Начальный строка ссылки.</span><span class="sxs-lookup"><span data-stu-id="88c76-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="88c76-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="88c76-110">_rwLast_</span></span>
  
<span data-ttu-id="88c76-111">Конечная строка ссылки.</span><span class="sxs-lookup"><span data-stu-id="88c76-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="88c76-112">Строка аргументов с отсчетом от нуля, соответствующая строка 1 передается как 0.</span><span class="sxs-lookup"><span data-stu-id="88c76-112">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="88c76-113">В Microsoft Office Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 65 535 = 2 ^ 16-1, а — максимальное значение, которое может быть занято WORD integer.</span><span class="sxs-lookup"><span data-stu-id="88c76-113">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="88c76-114">Начиная с версии Excel 2007 под управлением книги, максимальное значение — 1 048 575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="88c76-114">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="88c76-115">RW определяется как 32-разрядное целое число со знаком в XLCALL. З.</span><span class="sxs-lookup"><span data-stu-id="88c76-115">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="88c76-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="88c76-116">_colFirst_</span></span>
  
<span data-ttu-id="88c76-117">Начальный номер столбца ссылки.</span><span class="sxs-lookup"><span data-stu-id="88c76-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="88c76-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="88c76-118">_colLast_</span></span>
  
<span data-ttu-id="88c76-119">Последний номер столбца ссылки.</span><span class="sxs-lookup"><span data-stu-id="88c76-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="88c76-120">Столбец аргументы являются с отсчетом от нуля, поэтому этот столбец A передается как 0.</span><span class="sxs-lookup"><span data-stu-id="88c76-120">Column arguments are zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="88c76-121">В Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 255 = 2 ^ 8-1, а — максимальное значение, которое может быть занято БАЙТОВОЕ целое число.</span><span class="sxs-lookup"><span data-stu-id="88c76-121">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="88c76-122">Начиная с версии Excel 2007 под управлением книги, максимальное значение — 16,383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="88c76-122">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="88c76-123">Столбец — это 32-разрядное целое число со знаком в XLCALL. З.</span><span class="sxs-lookup"><span data-stu-id="88c76-123">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="88c76-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="88c76-124">Return value</span></span>

<span data-ttu-id="88c76-125">Возвращает **xltypeRef** внешняя ссылка прямоугольный блок ячеек, переданные в.</span><span class="sxs-lookup"><span data-stu-id="88c76-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="88c76-126">Пример</span><span class="sxs-lookup"><span data-stu-id="88c76-126">Example</span></span>

<span data-ttu-id="88c76-127">В этом примере функция **TempActiveRef12** используется для выбора A105:C110 ячеек.</span><span class="sxs-lookup"><span data-stu-id="88c76-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="88c76-128">См. также</span><span class="sxs-lookup"><span data-stu-id="88c76-128">See also</span></span>



[<span data-ttu-id="88c76-129">Функции в библиотеке Framework</span><span class="sxs-lookup"><span data-stu-id="88c76-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

