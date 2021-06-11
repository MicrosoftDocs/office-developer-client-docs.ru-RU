---
title: Функции из универсальной библиотеки DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- общие dll [Excel 2007], функции,функции [Excel 2007], Общий DLL
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
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="547d9-104">Функции из универсальной библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="547d9-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="547d9-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="547d9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="547d9-106">Папка содержит Microsoft Visual Studio и исходные файлы кода, необходимые для компиляции примера `\EXAMPLES\GENERIC\` DLL GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="547d9-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="547d9-107">Этот проект можно использовать в качестве шаблона для написания собственных Microsoft Excel XLLs.</span><span class="sxs-lookup"><span data-stu-id="547d9-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="547d9-108">Исходный код этого проекта демонстрирует многие функции API Excel C.</span><span class="sxs-lookup"><span data-stu-id="547d9-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="547d9-109">При загрузке GENERIC.xll создается новое **общее** меню с четырьмя командами:</span><span class="sxs-lookup"><span data-stu-id="547d9-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="547d9-110">**Диалоговое** окно . Отображает Microsoft Excel диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="547d9-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="547d9-111">**Dance** — перемещает выбор до нажатия **клавиши ESC.**</span><span class="sxs-lookup"><span data-stu-id="547d9-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="547d9-112">**Диалоговое окно** Native — отображает Windows диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="547d9-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="547d9-113">**Exit** — разгружает GENERIC.xll и удаляет **общее** меню.</span><span class="sxs-lookup"><span data-stu-id="547d9-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="547d9-114">GENERIC.xll также предоставляет три функции таблицы: Func1, FuncSum и FuncFib, которые можно использовать при загрузке GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="547d9-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="547d9-115">GENERIC.xll можно загрузить с помощью диспетчера надстройки или загрузить, если она была активна в обычном конце последнего сеанса Excel.</span><span class="sxs-lookup"><span data-stu-id="547d9-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="547d9-116">В этом проекте используется библиотека фреймворков (FRMWRK32.lib).</span><span class="sxs-lookup"><span data-stu-id="547d9-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="547d9-117">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="547d9-117">In this section</span></span>

[<span data-ttu-id="547d9-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="547d9-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="547d9-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="547d9-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="547d9-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="547d9-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="547d9-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="547d9-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="547d9-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="547d9-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="547d9-123">fDance</span><span class="sxs-lookup"><span data-stu-id="547d9-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="547d9-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="547d9-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="547d9-125">fExit</span><span class="sxs-lookup"><span data-stu-id="547d9-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="547d9-126">Func1</span><span class="sxs-lookup"><span data-stu-id="547d9-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="547d9-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="547d9-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="547d9-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="547d9-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="547d9-129">См. также</span><span class="sxs-lookup"><span data-stu-id="547d9-129">See also</span></span>



[<span data-ttu-id="547d9-130">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="547d9-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

