---
title: Функции в библиотеке платформы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- функции библиотеки Framework [excel 2007], функции [Excel 2007] библиотеки Framework
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807270"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="44ac5-104">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="44ac5-104">Functions in the Framework Library</span></span>

<span data-ttu-id="44ac5-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="44ac5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="44ac5-106">Чтобы обеспечить создание XLL-модулей для упрощения был создан библиотеки Framework.</span><span class="sxs-lookup"><span data-stu-id="44ac5-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="44ac5-107">Включает простой функции для управления **XLOPER**/ **XLOPER12** памяти, создание временной **XLOPER**/ **XLOPER12**, надежно вызов функции обратного вызова Microsoft Excel (**Excel4**, **Excel4v** ** Excel12 **, ** Excel12v **) и отладки строк на подключенного терминала печати.</span><span class="sxs-lookup"><span data-stu-id="44ac5-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, ** Excel12 **, ** Excel12v **) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="44ac5-108">Функции, включенные в этой библиотеке облегчить фрагмент кода, выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="44ac5-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="44ac5-109">Упрощенная код выглядит как следующий пример.</span><span class="sxs-lookup"><span data-stu-id="44ac5-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="44ac5-110">В библиотеке Framework включены следующие функции:</span><span class="sxs-lookup"><span data-stu-id="44ac5-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="44ac5-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="44ac5-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="44ac5-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="44ac5-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="44ac5-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="44ac5-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="44ac5-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="44ac5-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="44ac5-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="44ac5-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="44ac5-116">**Функции, используемые с XLOPERs**</span><span class="sxs-lookup"><span data-stu-id="44ac5-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="44ac5-117">**Функции, используемые с XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="44ac5-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44ac5-118">Excel</span><span class="sxs-lookup"><span data-stu-id="44ac5-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="44ac5-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="44ac5-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="44ac5-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="44ac5-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="44ac5-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="44ac5-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="44ac5-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="44ac5-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="44ac5-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="44ac5-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="44ac5-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="44ac5-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="44ac5-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="44ac5-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="44ac5-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="44ac5-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="44ac5-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="44ac5-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="44ac5-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="44ac5-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="44ac5-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="44ac5-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="44ac5-130">TempErr</span><span class="sxs-lookup"><span data-stu-id="44ac5-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="44ac5-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="44ac5-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="44ac5-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="44ac5-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="44ac5-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="44ac5-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="44ac5-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="44ac5-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="44ac5-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="44ac5-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="44ac5-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="44ac5-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="44ac5-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="44ac5-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="44ac5-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="44ac5-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="44ac5-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="44ac5-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="44ac5-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="44ac5-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="44ac5-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="44ac5-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="44ac5-142">Использование этих функций сокращает время, необходимое для записи DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="44ac5-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="44ac5-143">Начало разработки в моем приложении УНИВЕРСАЛЬНЫЙ также сокращает время разработки.</span><span class="sxs-lookup"><span data-stu-id="44ac5-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="44ac5-144">Использование УНИВЕРСАЛЬНЫХ. C как шаблон для настройки framework XLL-модуль и затем замените существующий код на свой.</span><span class="sxs-lookup"><span data-stu-id="44ac5-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="44ac5-145">Временные **XLOPER**/ **XLOPER12** функции создать **XLOPER**/ **XLOPER12** значения с помощью памяти из локального кучи управляется библиотеки Framework.</span><span class="sxs-lookup"><span data-stu-id="44ac5-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="44ac5-146">**XLOPER**/ **XLOPER12** значения остаются действительными до вызова функции **FreeAllTempMemory** или любой из функции **Excel** или **Excel12f** .</span><span class="sxs-lookup"><span data-stu-id="44ac5-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="44ac5-147">(Функции **Excel** и **Excel12f** освободить память все временные перед возвращением.)</span><span class="sxs-lookup"><span data-stu-id="44ac5-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="44ac5-148">Чтобы использовать функции библиотеки Framework, необходимо включить FRAMEWRK. H в коде C и добавьте FRAMEWRK. C или FRMWRK32. Файлы LIB в проект кода.</span><span class="sxs-lookup"><span data-stu-id="44ac5-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44ac5-149">См. также</span><span class="sxs-lookup"><span data-stu-id="44ac5-149">See also</span></span>

- [<span data-ttu-id="44ac5-150">Справочник по функциям API SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="44ac5-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

