---
title: Сведения об окне трассировки формул
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: Окно трассировки формул предназначено для предоставления разработчикам фигур сведений о взаимозависимостях ячеек — как зависимых ячеек (ячейках, зависящих от заданной ячейки), так и влияющих ячеек (ячеек, от которых зависит данная ячейка).
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345330"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="d0240-103">Сведения об окне трассировки формул</span><span class="sxs-lookup"><span data-stu-id="d0240-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="d0240-104">Окно **трассировки формул** предназначено для предоставления разработчикам фигур сведений о взаимозависимостях ячеек — как зависимых ячеек (ячейках, зависящих от заданной ячейки), так и влияющих ячеек (ячеек, от которых зависит данная ячейка).</span><span class="sxs-lookup"><span data-stu-id="d0240-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="d0240-105">В ячейках таблицы свойств фигуры Microsoft Visio содержатся значения и формулы.</span><span class="sxs-lookup"><span data-stu-id="d0240-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="d0240-106">Формулы могут, в свою очередь, содержать ссылки на другие ячейки, предоставляя возможность вычислить значение в одной ячейке на основе значения другой ячейки.</span><span class="sxs-lookup"><span data-stu-id="d0240-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="d0240-107">Однако при создании или поддержке сложных фигур может быть трудно определить все эти взаимозависимости, так как формула может ссылаться на любую ячейку в документе, независимо от того, является ли она ячейкой в той же таблице свойств фигуры, или ячейкой, принадлежащей другому объекту в документе, например, к странице, стилю, образцу или другой фигуре.</span><span class="sxs-lookup"><span data-stu-id="d0240-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="d0240-108">Окно **Трассировка формул** содержит сведения, которые помогут вам оценить последствия изменений, внесенных в ячейки.</span><span class="sxs-lookup"><span data-stu-id="d0240-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="d0240-109">Отображение окна трассировки формул</span><span class="sxs-lookup"><span data-stu-id="d0240-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="d0240-110">Чтобы просмотреть окно **трассировки формул** , а окно таблицы свойств фигуры является активным, в разделе **инструменты таблицы свойств фигуры** на вкладке \* \* Дизайн \* \* в группе **Трассировка формул** щелкните **Показать окно**.</span><span class="sxs-lookup"><span data-stu-id="d0240-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="d0240-111">По умолчанию окно **трассировки формулы** отображается закрепленным в окне таблицы свойств фигуры, но это закрепленное окно, которое можно прикрепить, поверх или объединить с другими доступными закрепленными окнами таблицы свойств фигуры, например, окно " **Обозреватель стилей** ".</span><span class="sxs-lookup"><span data-stu-id="d0240-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="d0240-112">Отслеживание зависимых ячеек</span><span class="sxs-lookup"><span data-stu-id="d0240-112">Tracing dependent cells</span></span>

<span data-ttu-id="d0240-113">Чтобы просмотреть список ячеек, зависящих от определенной ячейки, выберите эту ячейку в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d0240-113">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window.</span></span> <span data-ttu-id="d0240-114">В этом примере выбрана ячейка Width.</span><span class="sxs-lookup"><span data-stu-id="d0240-114">In this example, the Width cell is selected.</span></span> 
  
![Выбрана ячейка "ширина"](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="d0240-116">Чтобы просмотреть зависимые ячейки, в группе **Трассировка формул**щелкните **зависимости трассировки**.</span><span class="sxs-lookup"><span data-stu-id="d0240-116">To view its dependent cells, in the **Formula Tracing**group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="d0240-117">Список всех ячеек с зависимостью от ячейки ширина отображается в окне **Трассировка формул** .</span><span class="sxs-lookup"><span data-stu-id="d0240-117">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="d0240-118">Можно перейти к любой ячейке в списке, дважды щелкнув ее запись в окне **Трассировка формул** .</span><span class="sxs-lookup"><span data-stu-id="d0240-118">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Все ячейки с зависимостью от ячейки Width отображаются в окне Трассировка формул](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="d0240-120">Трассировка прецендентных ячеек</span><span class="sxs-lookup"><span data-stu-id="d0240-120">Tracing precendent cells</span></span>

<span data-ttu-id="d0240-121">Чтобы просмотреть список ячеек, от которых зависит определенная ячейка, сначала выберите ячейку в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d0240-121">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window.</span></span> <span data-ttu-id="d0240-122">В этом примере выбрана ячейка Geometry1. x2.</span><span class="sxs-lookup"><span data-stu-id="d0240-122">In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![Выбрана ячейка Geometry1. x2](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="d0240-124">Чтобы просмотреть влияющие ячейки, в группе **Трассировка формул**щелкните **влияющие**ячейки.</span><span class="sxs-lookup"><span data-stu-id="d0240-124">To view its precedent cells, in the **Formula Tracing**group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="d0240-125">Список всех ячеек, от которых зависит ячейка Geometry1. x2, отображается в окне **Трассировка формул** .</span><span class="sxs-lookup"><span data-stu-id="d0240-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="d0240-126">Можно перейти к любой ячейке в списке, дважды щелкнув ее запись в окне **Трассировка формул** .</span><span class="sxs-lookup"><span data-stu-id="d0240-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Все ячейки, от которых зависит ячейка Geometry1. x2, отображаются в окне Трассировка формул](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

