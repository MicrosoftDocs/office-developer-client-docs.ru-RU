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
- функция tempactivecolumn12 [excel 2007],Функция TempActiveColumn [Excel 2007]
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
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="bdc5a-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="bdc5a-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="bdc5a-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bdc5a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bdc5a-106">Функции библиотеки framework, которые создают временную **XLOPER12** /  **XLOPER12,** содержащую внешнюю ссылку на весь столбец активного листа.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="bdc5a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bdc5a-107">Parameters</span></span>

 <span data-ttu-id="bdc5a-108">_col_ (**BYTE)**</span><span class="sxs-lookup"><span data-stu-id="bdc5a-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="bdc5a-109">Столбец, на который следует ссылаться.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-109">The column to be referenced.</span></span> <span data-ttu-id="bdc5a-110">Это значение основано на нуле, поэтому столбец A передается как 0.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="bdc5a-111">В Microsoft Office Excel 2003 и более ранних версий, а начиная с Excel 2007, в котором книга работает в режиме совместимости, максимальное значение — 255 = 2^8 - 1 и это максимальное значение, которое может приниматься с помощью byTE-inte.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="bdc5a-112">Начиная с Excel 2007, где запущена книга, максимальное значение — 16 383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="bdc5a-113">COL определяется как 32-битное подписанное в XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="bdc5a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bdc5a-114">Return value</span></span>

<span data-ttu-id="bdc5a-115">Возвращает **внешнюю ссылку xltypeRef** на переданный столбец.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bdc5a-116">Пример</span><span class="sxs-lookup"><span data-stu-id="bdc5a-116">Example</span></span>

<span data-ttu-id="bdc5a-117">В следующем примере **tempActiveColumn12** используется для выбора всего столбца B.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="bdc5a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="bdc5a-118">See also</span></span>



[<span data-ttu-id="bdc5a-119">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="bdc5a-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

