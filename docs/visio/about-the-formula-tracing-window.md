---
title: О окне "Трассировка формул"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: Окно "Трассировка формул" предназначено для предоставления разработчикам фигур сведений о взаимозависимых ячейках — как зависимых ячейках (ячейках, зависимых от данной ячейки), так и о ячейках предыдущих размеров (от которых зависит данная ячейка).
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345330"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="08167-103">О окне "Трассировка формул"</span><span class="sxs-lookup"><span data-stu-id="08167-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="08167-104">Окно  "Трассировка формул" предназначено для предоставления разработчикам фигур сведений о взаимозависимых ячейках — как зависимых ячейках (ячейках, зависимых от данной ячейки), так и о ячейках предыдущих размеров (от которых зависит данная ячейка).</span><span class="sxs-lookup"><span data-stu-id="08167-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="08167-105">Ячейки в таблице фигур Microsoft Visio содержат значения и формулы.</span><span class="sxs-lookup"><span data-stu-id="08167-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="08167-106">Формулы, в свою очередь, могут иметь ссылки на другие ячейки, что дает вам возможность вычислять значение в одной ячейке на основе значения другой ячейки.</span><span class="sxs-lookup"><span data-stu-id="08167-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="08167-107">Однако при создании или обслуживании сложных фигур может быть трудно определить все эти взаимосвязи, так как формула может ссылаться на любую ячейку в рисунке, будь то ячейка в том же листе ShapeSheet или ячейка, принадлежащая другому объекту в рисунке, например страница, стиль, образец или другая фигура.</span><span class="sxs-lookup"><span data-stu-id="08167-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="08167-108">Окно **"Трассировка формул"** содержит сведения, которые помогут вам понять последствия изменений, внося в ячейки.</span><span class="sxs-lookup"><span data-stu-id="08167-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="08167-109">Отображение окна "Трассировка формул"</span><span class="sxs-lookup"><span data-stu-id="08167-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="08167-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span><span class="sxs-lookup"><span data-stu-id="08167-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="08167-111">Окно **"Трассировка** формул" по умолчанию закреплено в окне таблицы фигур, но является закрепленным окном, которое можно прикрепить, с  плавающей точкой или объединить с другими доступными закрепленными окнами таблицы фигур, например окном проводника стилей.</span><span class="sxs-lookup"><span data-stu-id="08167-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="08167-112">Трассировка зависимых ячеек</span><span class="sxs-lookup"><span data-stu-id="08167-112">Tracing dependent cells</span></span>

<span data-ttu-id="08167-113">Чтобы увидеть список ячеек, которые зависят от конкретной ячейки, выберите эту ячейку в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="08167-113">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window.</span></span> <span data-ttu-id="08167-114">В этом примере выбирается ячейка Width.</span><span class="sxs-lookup"><span data-stu-id="08167-114">In this example, the Width cell is selected.</span></span> 
  
![Выбрана ячейка Width](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="08167-116">Чтобы просмотреть зависимые ячейки, в группе **"Формула** трассировки" щелкните **"Зависимые трассировки".**</span><span class="sxs-lookup"><span data-stu-id="08167-116">To view its dependent cells, in the **Formula Tracing** group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="08167-117">Список всех ячеек с зависимостью от ячейки Width отображается в **окне "Трассировка формул".**</span><span class="sxs-lookup"><span data-stu-id="08167-117">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="08167-118">Можно перейти к любой ячейке в списке, дважды щелкнув ее запись в **окне "Трассировка формул".**</span><span class="sxs-lookup"><span data-stu-id="08167-118">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Все ячейки с зависимостью от ячейки Width отображаются в окне "Трассировка формул"](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="08167-120">Трассировка предочерепенных ячеек</span><span class="sxs-lookup"><span data-stu-id="08167-120">Tracing precendent cells</span></span>

<span data-ttu-id="08167-121">Чтобы увидеть список ячеек, от которые зависит определенная ячейка, сначала выберите ячейку в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="08167-121">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window.</span></span> <span data-ttu-id="08167-122">В этом примере выбрана ячейка Geometry1.X2.</span><span class="sxs-lookup"><span data-stu-id="08167-122">In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![Выбрана ячейка Geometry1.X2](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="08167-124">Чтобы просмотреть свои ячейки,в группе **"Трассировка** формул" щелкните **"Трассировка предыдущих".**</span><span class="sxs-lookup"><span data-stu-id="08167-124">To view its precedent cells, in the **Formula Tracing** group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="08167-125">Список всех ячеек, от которых зависит ячейка Geometry1.X2, отображается в **окне "Трассировка формул".**</span><span class="sxs-lookup"><span data-stu-id="08167-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="08167-126">Можно перейти к любой ячейке в списке, дважды щелкнув ее запись в **окне "Трассировка формул".**</span><span class="sxs-lookup"><span data-stu-id="08167-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Все ячейки, от которых зависит ячейка Geometry1.X2, отображаются в окне "Трассировка формул"](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

