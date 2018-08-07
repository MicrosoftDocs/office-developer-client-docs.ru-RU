---
title: Функции из универсальной библиотеки DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Универсальный dll [excel 2007], функции, функции [Excel 2007], универсальный DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807275"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="1759e-104">Функции из универсальной библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="1759e-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="1759e-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1759e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1759e-106">Папка `\EXAMPLES\GENERIC\` содержит файлы проекта Microsoft Visual Studio и файлы исходного кода, которые требуются для компиляции примера DLL GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="1759e-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="1759e-107">Можно использовать этот проект как шаблон для создания собственных XLL-модулей для Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1759e-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="1759e-108">Исходный код в этот проект демонстрирует многие функции интерфейса API для C Excel.</span><span class="sxs-lookup"><span data-stu-id="1759e-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="1759e-109">При загрузке GENERIC.xll, он создает новые **универсальные** меню с четырьмя командами:</span><span class="sxs-lookup"><span data-stu-id="1759e-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="1759e-110">**Диалоговое окно** - отображает диалоговое окно Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1759e-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="1759e-111">**Танец** - перемещается выделение только после нажатия клавиши **ESC** .</span><span class="sxs-lookup"><span data-stu-id="1759e-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="1759e-112">**Собственная диалогового окна** — отображает диалоговое окно Windows.</span><span class="sxs-lookup"><span data-stu-id="1759e-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="1759e-113">**Выход** - GENERIC.xll выгрузки и удаляет **универсальный** меню.</span><span class="sxs-lookup"><span data-stu-id="1759e-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="1759e-114">GENERIC.xll также предоставляет три функции листа, Func1, FuncSum и FuncFib, которую можно использовать при загрузке GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="1759e-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="1759e-115">GENERIC.xll можно загрузить с помощью диспетчера надстроек, или она загружается, если она была активна в конце обычной последнего сеанса Excel.</span><span class="sxs-lookup"><span data-stu-id="1759e-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="1759e-116">Этот проект использует библиотеку framework (FRMWRK32.lib).</span><span class="sxs-lookup"><span data-stu-id="1759e-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="1759e-117">В этой статье</span><span class="sxs-lookup"><span data-stu-id="1759e-117">In this section</span></span>

[<span data-ttu-id="1759e-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="1759e-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="1759e-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="1759e-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="1759e-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="1759e-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="1759e-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="1759e-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="1759e-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="1759e-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="1759e-123">fDance</span><span class="sxs-lookup"><span data-stu-id="1759e-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="1759e-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="1759e-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="1759e-125">fExit</span><span class="sxs-lookup"><span data-stu-id="1759e-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="1759e-126">Func1</span><span class="sxs-lookup"><span data-stu-id="1759e-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="1759e-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="1759e-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="1759e-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="1759e-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="1759e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="1759e-129">See also</span></span>



[<span data-ttu-id="1759e-130">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="1759e-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

