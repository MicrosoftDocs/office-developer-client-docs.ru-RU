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
- функция tempactiverow [excel 2007], функция TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807319"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="9042d-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="9042d-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="9042d-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9042d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9042d-106">Функции библиотеки Framework, создайте временный **XLOPER**/ **XLOPER12** , содержащий внешняя ссылка всю строку на активном листе.</span><span class="sxs-lookup"><span data-stu-id="9042d-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="9042d-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="9042d-107">Parameters</span></span>

 <span data-ttu-id="9042d-108">_Строка_</span><span class="sxs-lookup"><span data-stu-id="9042d-108">_row_</span></span>
  
<span data-ttu-id="9042d-109">Ссылаться на строку.</span><span class="sxs-lookup"><span data-stu-id="9042d-109">The row to be referenced.</span></span> <span data-ttu-id="9042d-110">Строка аргументов с отсчетом от нуля, соответствующая строка 1 передается как 0.</span><span class="sxs-lookup"><span data-stu-id="9042d-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="9042d-111">В Microsoft Office Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 65 535 = 2 ^ 16-1, а — максимальное значение, которое может быть занято WORD integer.</span><span class="sxs-lookup"><span data-stu-id="9042d-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="9042d-112">Начиная с версии Excel 2007 под управлением книги, максимальное значение — 1 048 575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="9042d-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="9042d-113">RW определяется как 32-разрядное целое число со знаком в XLCALL. З.</span><span class="sxs-lookup"><span data-stu-id="9042d-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="9042d-114">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9042d-114">Return value</span></span>

<span data-ttu-id="9042d-115">Возвращает **xltypeRef** внешняя ссылка переданную ячейки строки.</span><span class="sxs-lookup"><span data-stu-id="9042d-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9042d-116">Пример</span><span class="sxs-lookup"><span data-stu-id="9042d-116">Example</span></span>

<span data-ttu-id="9042d-117">В этом примере функция **TempActiveRow12** используется для выбора строки 113.</span><span class="sxs-lookup"><span data-stu-id="9042d-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="9042d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="9042d-118">See also</span></span>



[<span data-ttu-id="9042d-119">Функции в библиотеке Framework</span><span class="sxs-lookup"><span data-stu-id="9042d-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

