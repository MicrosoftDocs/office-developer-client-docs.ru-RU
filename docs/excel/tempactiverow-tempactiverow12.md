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
- Функция темпактиверов [Excel 2007], функция TempActiveRow12 [Excel 2007]
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
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="0ec87-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="0ec87-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="0ec87-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0ec87-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0ec87-106">Функции библиотеки Framework, которые создают временную структуру **XLOPER**/ \*\*\*\* , содержащую внешнюю ссылку на всю строку на активном листе.</span><span class="sxs-lookup"><span data-stu-id="0ec87-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="0ec87-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ec87-107">Parameters</span></span>

 <span data-ttu-id="0ec87-108">_Строка_</span><span class="sxs-lookup"><span data-stu-id="0ec87-108">_row_</span></span>
  
<span data-ttu-id="0ec87-109">Строка, на которую необходимо сослаться.</span><span class="sxs-lookup"><span data-stu-id="0ec87-109">The row to be referenced.</span></span> <span data-ttu-id="0ec87-110">Аргументы строки отсчитываются от нуля, поэтому строка 1 передается как 0.</span><span class="sxs-lookup"><span data-stu-id="0ec87-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="0ec87-111">В Microsoft Office Excel 2003 и более ранних версиях, начиная с Excel 2007 Запуск книги в режиме совместимости, максимальное значение равно 65 535 = 2 ^ 16-1 и является максимальным значением, которое может принимать слово Integer.</span><span class="sxs-lookup"><span data-stu-id="0ec87-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="0ec87-112">Начиная с Excel 2007 Запуск книги, максимальное значение равно 1 048 575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="0ec87-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="0ec87-113">RW определяется как 32-разрядное целое число со знаком в XLCALL. Высоты.</span><span class="sxs-lookup"><span data-stu-id="0ec87-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="0ec87-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ec87-114">Return value</span></span>

<span data-ttu-id="0ec87-115">Возвращает внешнюю ссылку **кслтипереф** на переданные ячейки строк.</span><span class="sxs-lookup"><span data-stu-id="0ec87-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0ec87-116">Пример</span><span class="sxs-lookup"><span data-stu-id="0ec87-116">Example</span></span>

<span data-ttu-id="0ec87-117">В этом примере функция **TempActiveRow12** используется для выбора строки 113.</span><span class="sxs-lookup"><span data-stu-id="0ec87-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="0ec87-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0ec87-118">See also</span></span>



[<span data-ttu-id="0ec87-119">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="0ec87-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

