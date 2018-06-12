---
title: �������, ������� � ��������� Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- states [excel 2007],commands [Excel 2007],worksheet functions [Excel 2007],macro-sheet functions [Excel 2007],Excel states
localization_priority: Normal
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 60977216663fb2492f425a9b7c855b77815f0e7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807179"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="72a39-104">�������, ������� � ��������� Excel</span><span class="sxs-lookup"><span data-stu-id="72a39-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="72a39-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="72a39-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="72a39-106">� Microsoft Excel ����� ������������ ��� ����� ������ ���� �������������� ������������: ������� � �������.</span><span class="sxs-lookup"><span data-stu-id="72a39-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="72a39-107">�������</span><span class="sxs-lookup"><span data-stu-id="72a39-107">Commands</span></span>

<span data-ttu-id="72a39-108">�������������� ������ � Excel:</span><span class="sxs-lookup"><span data-stu-id="72a39-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="72a39-109">��� ��������� �������� ��� ��, ��� � ������������.</span><span class="sxs-lookup"><span data-stu-id="72a39-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="72a39-110">��� ����� ��� �� ��, ��� � ������������ (� ������ ����������� ������������� ����������). ��������, �������� ��������� Excel, �������� ��������, � ����� ���������, ��������� � ������������� ���������.</span><span class="sxs-lookup"><span data-stu-id="72a39-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="72a39-111">����� ��������� �� ����� ��� ������������� ������������ ������������� �������.</span><span class="sxs-lookup"><span data-stu-id="72a39-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="72a39-112">��� ����� ��������� ���������� ���� � ����������������� � �������������.</span><span class="sxs-lookup"><span data-stu-id="72a39-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="72a39-113">�� ����� ������� c ��������� ����������, ����� ��� ���������� ��� ���������� ������������ �������� ��� ���� ��������, �������� ��� ������ ����� ������� ����.</span><span class="sxs-lookup"><span data-stu-id="72a39-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="72a39-114">��� ������� �� ���������� � Excel �� ����� ���������.</span><span class="sxs-lookup"><span data-stu-id="72a39-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="72a39-115">�� �� ����� ������� ������� �� ����� ���������.</span><span class="sxs-lookup"><span data-stu-id="72a39-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="72a39-116">�������</span><span class="sxs-lookup"><span data-stu-id="72a39-116">Functions</span></span>

<span data-ttu-id="72a39-117">�������������� ������� � Excel:</span><span class="sxs-lookup"><span data-stu-id="72a39-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="72a39-118">������ ��� ����� ��������� � ������ ���������� ���������.</span><span class="sxs-lookup"><span data-stu-id="72a39-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="72a39-119">�� ����� �������� � ���� ��� ��������� ����� ��� ����� ������� Excel.</span><span class="sxs-lookup"><span data-stu-id="72a39-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="72a39-120">�� ����� ������������ � ������������ ����.</span><span class="sxs-lookup"><span data-stu-id="72a39-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="72a39-121">�� ����� ������������ � ���������� ��������� �������� � ����������� ��������� ��������������.</span><span class="sxs-lookup"><span data-stu-id="72a39-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="72a39-122">�� ����� �������� �������.</span><span class="sxs-lookup"><span data-stu-id="72a39-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="72a39-123">��� �� ����� �������� �������.</span><span class="sxs-lookup"><span data-stu-id="72a39-123">They cannot call commands.</span></span>
    
<span data-ttu-id="72a39-p101">����� ����, Excel ��������� ���������������� ������� ����� � ���������������� �������, ��������������� ��� ������ �� ������ ��������. ������������� ������� ����� �������� �� ���������� ������ ������� ��������: �� ����� ������������ ��� ��, ��� � ������� ������� �����.</span><span class="sxs-lookup"><span data-stu-id="72a39-p101">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets. Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="72a39-126">������� �����</span><span class="sxs-lookup"><span data-stu-id="72a39-126">Worksheet Functions</span></span>

<span data-ttu-id="72a39-127">�������������� ������� ����� � Excel:</span><span class="sxs-lookup"><span data-stu-id="72a39-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="72a39-128">��� �� ����� �������� ������ � �������������� �������� ����� ��������.</span><span class="sxs-lookup"><span data-stu-id="72a39-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="72a39-129">��� �� ����� �������� �������� ������������� �����.</span><span class="sxs-lookup"><span data-stu-id="72a39-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="72a39-130">�� ����� ���������� � �������������� ��� ����������������, ������� � Excel�2007.</span><span class="sxs-lookup"><span data-stu-id="72a39-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="72a39-131">������� ����� ��������</span><span class="sxs-lookup"><span data-stu-id="72a39-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="72a39-132">�������������� ������� ����� �������� � Excel:</span><span class="sxs-lookup"><span data-stu-id="72a39-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="72a39-133">��� ����� �������� ������ � �������������� �������� ����� ��������.</span><span class="sxs-lookup"><span data-stu-id="72a39-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="72a39-134">��� ����� �������� �������� ������������� �����, � ��� ����� �������� ���������� �����.</span><span class="sxs-lookup"><span data-stu-id="72a39-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="72a39-135">��� �� ��������� �����������������, ������� � Excel�2007.</span><span class="sxs-lookup"><span data-stu-id="72a39-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="72a39-p102">��� ���������������� ������� (UDF) ��������������, ����� ���������� ����� � ��� ��������������� � Excel � ��� ��� ������������ ��� �� �����������. ���� ������� ���������������� ��� ������� �����, �� ���������� ��������� ��������, ������� ����� ��������� ������ ������� ����� ��������, ���������� ���� ��������. ������� � Excel�2007, ���� ������� �����, ������������������ ��� ����������������, �������� ������� ������� ����� ��������, ���������� ���� ��������.</span><span class="sxs-lookup"><span data-stu-id="72a39-p102">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function. If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails. Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="72a39-139">� Excel ���������������� ������� Microsoft Visual Basic ��� ���������� (VBA) �������������� ���������� �������� ����� �������� � ��� �����, ��� ��� ����� �������� ������ � ��������� � ������� ������� � �������� ������������� �����, � ����� �� ��������� �����������������, ������� � Excel�2007.</span><span class="sxs-lookup"><span data-stu-id="72a39-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="72a39-140">��������� Excel</span><span class="sxs-lookup"><span data-stu-id="72a39-140">Excel States</span></span>

<span data-ttu-id="72a39-141">� ����� ������ ������� Excel ����� ���� � ����� �� ��������� ��������� � ����������� �� �������� ������������, �������� ��������, �������������� �������, ������������ ������, ��� ���������������� ���������� ������� Excel, �������� **Autosave**.</span><span class="sxs-lookup"><span data-stu-id="72a39-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="72a39-142">���������, ������������� ���������� ������������:</span><span class="sxs-lookup"><span data-stu-id="72a39-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="72a39-p103">**��������� ����������.** ������� � ������� �� �����������. ���������� ���� �� ������������. ������ �� �������������, ������������ �� ��������� �������� ���������, ����������� ��� �������. ���������� ������� �� ������������.</span><span class="sxs-lookup"><span data-stu-id="72a39-p103">**Ready state:** No commands or macros are being run. No dialog boxes are being displayed. No cells are being edited and the user is not in the middle of a cut/copy and paste operation. No embedded object has focus.</span></span> 
    
- <span data-ttu-id="72a39-147">**����� ��������������.** ������������ ����� ������� ���������� ������� � ����������������� ��� ������������ ������ ��� ����� ������� **F2**, ������� ���� ��� ��������� ����������������� ��� ������������ �����.</span><span class="sxs-lookup"><span data-stu-id="72a39-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="72a39-148">**����� ���������, ����������� ��� �������.** ������������ ������� ��� ���������� ������ ���� �������� ����� � ��� �� ������� �� (���� ������� ��, ��������� ���������� ���� "����������� �������", � ������� �������� ��������� �������� �������).</span><span class="sxs-lookup"><span data-stu-id="72a39-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="72a39-149">**����� ��������.** ������������ ����������� ������� � �������� ������, ������ ������� ����������� � ������������� �������.</span><span class="sxs-lookup"><span data-stu-id="72a39-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="72a39-p104">������������ ����� ����� �� ������� ��������������, ��������, ��������� ��� �����������, ����� ������� **ESC**, ����� ���� Excel �������� � ��������� ����������. ������ ������� ����� �������� ��� ���������, ��������:</span><span class="sxs-lookup"><span data-stu-id="72a39-p104">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state. Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="72a39-152">������������ ��������� ���������� ���������� ����.</span><span class="sxs-lookup"><span data-stu-id="72a39-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="72a39-153">������������ �������� ��������.</span><span class="sxs-lookup"><span data-stu-id="72a39-153">The user initiates a recalculation.</span></span>
    
- <span data-ttu-id="72a39-154">������������ ��������� �������.</span><span class="sxs-lookup"><span data-stu-id="72a39-154">The user runs a command.</span></span>
    
- <span data-ttu-id="72a39-155">Excel ��������� �������� **Autosave**.</span><span class="sxs-lookup"><span data-stu-id="72a39-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="72a39-156">��������������� ������� �������.</span><span class="sxs-lookup"><span data-stu-id="72a39-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="72a39-p105">��������� ������ ����� ��� ������������� ���������. ��������� � ���������� ������ ������� ��� ������� ������� ����� ��������� ���������� �� �������� ������������� Excel. ���� ��� �������� ���������� �����������, ���������� ������������ ������������� ������� ������ ������������� ��, ����� ��� ������������� ����� ���� �� ��������, ���������� � ��������� ��� ������.</span><span class="sxs-lookup"><span data-stu-id="72a39-p105">The last example is of importance to add-in developers. You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed. When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72a39-160">��. �����</span><span class="sxs-lookup"><span data-stu-id="72a39-160">See also</span></span>



[<span data-ttu-id="72a39-161">�������� ���������������� � Excel</span><span class="sxs-lookup"><span data-stu-id="72a39-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="72a39-162">���������� ������������ �������� ������� � ���������� ��������</span><span class="sxs-lookup"><span data-stu-id="72a39-162">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)

