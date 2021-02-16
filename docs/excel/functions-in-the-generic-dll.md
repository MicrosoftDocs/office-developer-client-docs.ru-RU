---
title: Функции из универсальной библиотеки DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420600"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="787b8-104">Функции из универсальной библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="787b8-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="787b8-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="787b8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="787b8-106">Папка содержит файлы проектов Microsoft Visual Studio и файлы исходных кодов, необходимые для компиляции примера  `\EXAMPLES\GENERIC\` DLL GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="787b8-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="787b8-107">Этот проект можно использовать в качестве шаблона для написания собственных XLL Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="787b8-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="787b8-108">Исходный код в этом проекте демонстрирует многие функции API C для Excel.</span><span class="sxs-lookup"><span data-stu-id="787b8-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="787b8-109">При загрузке GENERIC.xll создается новое **универсальное** меню с четырьмя командами:</span><span class="sxs-lookup"><span data-stu-id="787b8-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="787b8-110">**Диалоговое окно** — отображает диалоговое окно Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="787b8-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="787b8-111">**1** — перемещает выделение, пока не нажать клавишу **ESC.**</span><span class="sxs-lookup"><span data-stu-id="787b8-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="787b8-112">**Диалоговое окно Native** — отображает диалоговое окно Windows.</span><span class="sxs-lookup"><span data-stu-id="787b8-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="787b8-113">**Exit** — выгружает GENERIC.xll и удаляет **универсальное** меню.</span><span class="sxs-lookup"><span data-stu-id="787b8-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="787b8-114">GENERIC.xll также предоставляет три функции таблицы, Func1, FuncSum и FuncFib, которые можно использовать при загрузке GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="787b8-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="787b8-115">GENERIC.xll можно загрузить с помощью диспетчера надстройки или загрузить, если он был активен в обычном конце последнего сеанса Excel.</span><span class="sxs-lookup"><span data-stu-id="787b8-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="787b8-116">Этот проект использует библиотеку структуры (FRMWRK32.lib).</span><span class="sxs-lookup"><span data-stu-id="787b8-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="787b8-117">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="787b8-117">In this section</span></span>

[<span data-ttu-id="787b8-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="787b8-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="787b8-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="787b8-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="787b8-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="787b8-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="787b8-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="787b8-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="787b8-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="787b8-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="787b8-123">fDance</span><span class="sxs-lookup"><span data-stu-id="787b8-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="787b8-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="787b8-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="787b8-125">fExit</span><span class="sxs-lookup"><span data-stu-id="787b8-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="787b8-126">Func1</span><span class="sxs-lookup"><span data-stu-id="787b8-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="787b8-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="787b8-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="787b8-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="787b8-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="787b8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="787b8-129">See also</span></span>



[<span data-ttu-id="787b8-130">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="787b8-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

