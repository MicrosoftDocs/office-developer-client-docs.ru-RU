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
- Функция TempActiveCell12 [Excel 2007], функция Темпактивецелл [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301577"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="04d83-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="04d83-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="04d83-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="04d83-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="04d83-106">Функции библиотеки Framework, которые создают временную структуру **XLOPER**/ \*\*\*\* , содержащую внешнюю ссылку на ячейку на активном листе.</span><span class="sxs-lookup"><span data-stu-id="04d83-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="04d83-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="04d83-107">Parameters</span></span>

 <span data-ttu-id="04d83-108">_Строка_</span><span class="sxs-lookup"><span data-stu-id="04d83-108">_row_</span></span>
  
<span data-ttu-id="04d83-109">Строка, на которую необходимо сослаться.</span><span class="sxs-lookup"><span data-stu-id="04d83-109">The row to be referenced.</span></span> <span data-ttu-id="04d83-110">Аргументы строки отсчитываются от нуля, поэтому строка 1 передается как 0.</span><span class="sxs-lookup"><span data-stu-id="04d83-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="04d83-111">В Microsoft Office Excel 2003 и более ранних версиях, начиная с Excel 2007 Запуск книги в режиме совместимости, максимальное значение равно 65 535 = 2 ^ 16-1 и является максимальным значением, которое может принимать слово Integer.</span><span class="sxs-lookup"><span data-stu-id="04d83-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="04d83-112">Начиная с Excel 2007 Запуск книги, максимальное значение равно 1 048 575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="04d83-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="04d83-113">RW определяется как 32-разрядное целое число со знаком в XLCALL. Высоты.</span><span class="sxs-lookup"><span data-stu-id="04d83-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="04d83-114">_столбца_</span><span class="sxs-lookup"><span data-stu-id="04d83-114">_col_</span></span>
  
<span data-ttu-id="04d83-115">Столбец, на который необходимо сослаться.</span><span class="sxs-lookup"><span data-stu-id="04d83-115">The column to be referenced.</span></span> <span data-ttu-id="04d83-116">Это отсчитывается от нуля, поэтому столбец A передается как 0.</span><span class="sxs-lookup"><span data-stu-id="04d83-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="04d83-117">В Excel 2003 и более ранних версиях, начиная с Excel 2007 выполнение книги в режиме совместимости, максимальное значение равно 255 = 2 ^ 8-1 и является максимальным значением, которое может быть получено с помощью БАЙТового целого числа.</span><span class="sxs-lookup"><span data-stu-id="04d83-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="04d83-118">Начиная с Excel 2007 Запуск книги, максимальное значение равно 16 383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="04d83-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="04d83-119">COL определен как 32-разрядное целое число со знаком в XLCALL. Высоты.</span><span class="sxs-lookup"><span data-stu-id="04d83-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="04d83-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04d83-120">Return value</span></span>

<span data-ttu-id="04d83-121">Возвращает внешнюю ссылку **кслтипереф** на переданную ячейку.</span><span class="sxs-lookup"><span data-stu-id="04d83-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="04d83-122">Пример</span><span class="sxs-lookup"><span data-stu-id="04d83-122">Example</span></span>

<span data-ttu-id="04d83-123">В следующем примере используется **TempActiveCell12** для отображения содержимого B94 на активном листе.</span><span class="sxs-lookup"><span data-stu-id="04d83-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="04d83-124">См. также</span><span class="sxs-lookup"><span data-stu-id="04d83-124">See also</span></span>



[<span data-ttu-id="04d83-125">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="04d83-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

