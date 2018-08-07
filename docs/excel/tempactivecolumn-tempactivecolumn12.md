---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- функция tempactivecolumn12 [excel 2007], функция TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807324"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="a2c0f-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="a2c0f-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="a2c0f-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a2c0f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a2c0f-106">Функции библиотеки Framework, создайте временный **XLOPER**/ **XLOPER12** , содержащий внешняя ссылка на целый столбец на активном листе.</span><span class="sxs-lookup"><span data-stu-id="a2c0f-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="a2c0f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2c0f-107">Parameters</span></span>

 <span data-ttu-id="a2c0f-108">_столбец_ (**БАЙТ**)</span><span class="sxs-lookup"><span data-stu-id="a2c0f-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="a2c0f-109">Ссылка на столбец.</span><span class="sxs-lookup"><span data-stu-id="a2c0f-109">The column to be referenced.</span></span> <span data-ttu-id="a2c0f-110">Это с отсчетом от нуля, поэтому этот столбец A передается как 0.</span><span class="sxs-lookup"><span data-stu-id="a2c0f-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="a2c0f-111">В Microsoft Office Excel 2003 и более ранних версий, а начиная с версии Excel 2007, выполнение книги в режиме совместимости, максимальное значение — 255 = 2 ^ 8-1, а — максимальное значение, которое может быть занято БАЙТОВОЕ целое число.</span><span class="sxs-lookup"><span data-stu-id="a2c0f-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="a2c0f-112">Начиная с версии Excel 2007 под управлением книги, максимальное значение — 16,383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="a2c0f-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="a2c0f-113">Столбец — это 32-разрядное целое число со знаком в XLCALL. З.</span><span class="sxs-lookup"><span data-stu-id="a2c0f-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a2c0f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="a2c0f-115">Возвращает **xltypeRef** внешняя ссылка на столбец, переданные в.</span><span class="sxs-lookup"><span data-stu-id="a2c0f-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a2c0f-116">Пример</span><span class="sxs-lookup"><span data-stu-id="a2c0f-116">Example</span></span>

<span data-ttu-id="a2c0f-117">В следующем примере используется **TempActiveColumn12** для выбора целый столбец б.</span><span class="sxs-lookup"><span data-stu-id="a2c0f-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a2c0f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a2c0f-118">See also</span></span>



[<span data-ttu-id="a2c0f-119">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="a2c0f-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

