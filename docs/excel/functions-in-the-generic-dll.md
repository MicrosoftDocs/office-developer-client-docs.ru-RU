---
title: Функции из универсальной библиотеки DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- универсальная библиотека DLL [Excel 2007], функции, функции [Excel 2007], Общая библиотека DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304090"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="717bd-104">Функции из универсальной библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="717bd-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="717bd-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="717bd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="717bd-106">В этой `\EXAMPLES\GENERIC\` папке содержатся файлы проекта Microsoft Visual Studio и файлы исходного кода, необходимые для компиляции примера GENERIC DLL Generic. XLL.</span><span class="sxs-lookup"><span data-stu-id="717bd-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="717bd-107">Вы можете использовать этот проект в качестве шаблона для создания собственных XLL Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="717bd-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="717bd-108">Исходный код в этом проекте демонстрирует многие функции API C для Excel.</span><span class="sxs-lookup"><span data-stu-id="717bd-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="717bd-109">При загрузке GENERIC. XLL создается новое универсальное меню с \*\*\*\* четырьмя командами:</span><span class="sxs-lookup"><span data-stu-id="717bd-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="717bd-110">**ДиалоговОе окно** — отображает диалоговое окно Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="717bd-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="717bd-111">**Данце** — выделяет выделенный фрагмент, пока вы не нажмете клавишу **ESC** .</span><span class="sxs-lookup"><span data-stu-id="717bd-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="717bd-112">**Собственное диалоговОе окно** — отображает диалоговое окно Windows.</span><span class="sxs-lookup"><span data-stu-id="717bd-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="717bd-113">**Exit** — выгружает Generic. XLL и удаляет **Общее** меню.</span><span class="sxs-lookup"><span data-stu-id="717bd-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="717bd-114">GENERIC. XLL также предоставляет три функции листа, func1, Функсум и Функфиб, которые можно использовать каждый раз, когда загружается GENERIC. XLL.</span><span class="sxs-lookup"><span data-stu-id="717bd-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="717bd-115">GENERIC. XLL можно загрузить с помощью диспетчера надстроек или загрузить, если она была активна в обычном конце последнего сеанса Excel.</span><span class="sxs-lookup"><span data-stu-id="717bd-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="717bd-116">В этом проекте используется библиотека Framework (FRMWRK32. lib).</span><span class="sxs-lookup"><span data-stu-id="717bd-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="717bd-117">Содержание</span><span class="sxs-lookup"><span data-stu-id="717bd-117">In this section</span></span>

[<span data-ttu-id="717bd-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="717bd-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="717bd-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="717bd-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="717bd-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="717bd-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="717bd-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="717bd-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="717bd-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="717bd-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="717bd-123">fDance</span><span class="sxs-lookup"><span data-stu-id="717bd-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="717bd-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="717bd-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="717bd-125">fExit</span><span class="sxs-lookup"><span data-stu-id="717bd-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="717bd-126">Func1</span><span class="sxs-lookup"><span data-stu-id="717bd-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="717bd-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="717bd-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="717bd-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="717bd-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="717bd-129">См. также</span><span class="sxs-lookup"><span data-stu-id="717bd-129">See also</span></span>



[<span data-ttu-id="717bd-130">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="717bd-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

