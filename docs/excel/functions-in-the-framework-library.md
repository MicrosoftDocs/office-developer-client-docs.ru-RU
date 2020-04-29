---
title: Функции в библиотеке платформы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- функции библиотеки Framework [Excel 2007], функции [Excel 2007], Библиотека Framework
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417548"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="7804c-104">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="7804c-104">Functions in the Framework Library</span></span>

<span data-ttu-id="7804c-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7804c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7804c-106">Библиотека Framework была создана для упрощения создания XLL.</span><span class="sxs-lookup"><span data-stu-id="7804c-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="7804c-107">Он включает в себя простые функции для управления памятью для **XLOPER**/ **XLOPER12** , **Создание временной**/ **XLOPER12**, надежный вызов функций обратного вызова Microsoft Excel (**Excel4**, **Excel4v**, \* \* Excel12 \* \*, \* \* Excel12v \* \*) и печать строк отладки на подключенном терминале.</span><span class="sxs-lookup"><span data-stu-id="7804c-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, \*\* Excel12 \*\*, \*\* Excel12v \*\*) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="7804c-108">Функции, включенные в эту библиотеку, помогают упростить фрагмент кода, который выглядит примерно так:</span><span class="sxs-lookup"><span data-stu-id="7804c-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="7804c-109">Упрощенный код выглядит так, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="7804c-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="7804c-110">В библиотеку Framework включены следующие функции:</span><span class="sxs-lookup"><span data-stu-id="7804c-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="7804c-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="7804c-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="7804c-112">**жеттемпмемори**</span><span class="sxs-lookup"><span data-stu-id="7804c-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="7804c-113">**фриаллтемпмемори**</span><span class="sxs-lookup"><span data-stu-id="7804c-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="7804c-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="7804c-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="7804c-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="7804c-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="7804c-116">**Функции, используемые с XLOPER**</span><span class="sxs-lookup"><span data-stu-id="7804c-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="7804c-117">**Функции, используемые с XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="7804c-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7804c-118">Excel</span><span class="sxs-lookup"><span data-stu-id="7804c-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="7804c-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="7804c-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="7804c-120">темпнум</span><span class="sxs-lookup"><span data-stu-id="7804c-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="7804c-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="7804c-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="7804c-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="7804c-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="7804c-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="7804c-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="7804c-124">темпстрконст</span><span class="sxs-lookup"><span data-stu-id="7804c-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="7804c-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="7804c-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="7804c-126">темпбул</span><span class="sxs-lookup"><span data-stu-id="7804c-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="7804c-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="7804c-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="7804c-128">темпинт</span><span class="sxs-lookup"><span data-stu-id="7804c-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="7804c-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="7804c-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="7804c-130">темперр</span><span class="sxs-lookup"><span data-stu-id="7804c-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="7804c-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="7804c-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="7804c-132">темпактивереф</span><span class="sxs-lookup"><span data-stu-id="7804c-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="7804c-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="7804c-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="7804c-134">темпактивецелл</span><span class="sxs-lookup"><span data-stu-id="7804c-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="7804c-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="7804c-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="7804c-136">темпактиверов</span><span class="sxs-lookup"><span data-stu-id="7804c-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="7804c-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="7804c-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="7804c-138">темпактивеколумн</span><span class="sxs-lookup"><span data-stu-id="7804c-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="7804c-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="7804c-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="7804c-140">темпмиссинг</span><span class="sxs-lookup"><span data-stu-id="7804c-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="7804c-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="7804c-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="7804c-142">Использование этих функций сокращает количество времени, необходимого для записи DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="7804c-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="7804c-143">Запуск разработки из примера УНИВЕРСАЛЬНого приложения также сокращает время разработки.</span><span class="sxs-lookup"><span data-stu-id="7804c-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="7804c-144">Используйте GENERIC. C в качестве шаблона для помощи в настройке платформы XLL, а затем замените существующий код на свой собственный.</span><span class="sxs-lookup"><span data-stu-id="7804c-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="7804c-145">Функции Temporary **XLOPER**/ **XLOPER12** создают значения **XLOPER**/ **XLOPER12** , используя память из локальной кучи, управляемой библиотекой Framework.</span><span class="sxs-lookup"><span data-stu-id="7804c-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="7804c-146">Значения параметра **XLOPER**/ **XLOPER12** действуют до тех пор, пока не будет вызвана функция **фриаллтемпмемори** или обе функции **Excel** или **Excel12f** .</span><span class="sxs-lookup"><span data-stu-id="7804c-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="7804c-147">(В **Excel** и **Excel12f** функции освобождают всю временную память перед возвратом.)</span><span class="sxs-lookup"><span data-stu-id="7804c-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="7804c-148">Чтобы использовать функции библиотеки Framework, необходимо включить FRAMEWRK. H в коде C и добавление FRAMEWRK. C или FRMWRK32. LIB файлы в проект кода.</span><span class="sxs-lookup"><span data-stu-id="7804c-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7804c-149">См. также</span><span class="sxs-lookup"><span data-stu-id="7804c-149">See also</span></span>

- [<span data-ttu-id="7804c-150">Справочник по функциям API SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="7804c-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

