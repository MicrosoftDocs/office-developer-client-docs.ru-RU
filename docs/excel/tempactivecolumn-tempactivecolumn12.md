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
- функция tempactivecolumn12 [Excel 2007], функция TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417877"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="3fd9a-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="3fd9a-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="3fd9a-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3fd9a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3fd9a-106">Функции библиотеки Framework, создав временную **XLOPER XLOPER12,** содержащую внешнюю ссылку на весь столбец /   на активном листе.</span><span class="sxs-lookup"><span data-stu-id="3fd9a-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="3fd9a-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="3fd9a-107">Parameters</span></span>

 <span data-ttu-id="3fd9a-108">_col_ **(BYTE)**</span><span class="sxs-lookup"><span data-stu-id="3fd9a-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="3fd9a-109">Столбец, на который следует ссылаться.</span><span class="sxs-lookup"><span data-stu-id="3fd9a-109">The column to be referenced.</span></span> <span data-ttu-id="3fd9a-110">Это нулевое значение, поэтому столбец A передается в качестве 0.</span><span class="sxs-lookup"><span data-stu-id="3fd9a-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="3fd9a-111">В Microsoft Office Excel 2003 г. и более ранних версиях и начиная с Excel 2007 г. при запуске книги в режиме совместимости максимальное значение — 255 = 2^8 — 1 и является максимальным значением, которое может приниматься в integer BYTE.</span><span class="sxs-lookup"><span data-stu-id="3fd9a-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="3fd9a-112">Начиная с Excel 2007 года при запуске книги максимальное значение — 16 383 = 2^14 — 1.</span><span class="sxs-lookup"><span data-stu-id="3fd9a-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="3fd9a-113">COL определяется как 32-битный подписанный в XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="3fd9a-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3fd9a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3fd9a-114">Return value</span></span>

<span data-ttu-id="3fd9a-115">Возвращает **внешнюю ссылку xltypeRef** на переданный столбец.</span><span class="sxs-lookup"><span data-stu-id="3fd9a-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3fd9a-116">Пример</span><span class="sxs-lookup"><span data-stu-id="3fd9a-116">Example</span></span>

<span data-ttu-id="3fd9a-117">В следующем примере **tempActiveColumn12** используется для выбора всего столбца B.</span><span class="sxs-lookup"><span data-stu-id="3fd9a-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="3fd9a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="3fd9a-118">See also</span></span>



[<span data-ttu-id="3fd9a-119">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="3fd9a-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

