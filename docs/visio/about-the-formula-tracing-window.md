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
description: Окно трассировки формул предназначенный для разработчиков фигуры со сведениями о взаимозависимости ячейки, зависимые ячейки (ячейки с зависимостями в указанной ячейке) и влияющие ячейки (ячейки, от которых зависит указанной ячейке).
ms.openlocfilehash: 316ac219f548b2459ea2d0ad8cece0f693957fcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813115"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="441f8-103">Сведения об окне трассировки формул</span><span class="sxs-lookup"><span data-stu-id="441f8-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="441f8-104">Окно **Трассировки формул** предназначенный для разработчиков фигуры со сведениями о взаимозависимости ячейки, зависимые ячейки (ячейки с зависимостями в указанной ячейке) и влияющие ячейки (ячейки, от которых зависит указанной ячейке).</span><span class="sxs-lookup"><span data-stu-id="441f8-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="441f8-105">Ячейки в Microsoft Visio ShapeSheet содержат значения и формулы.</span><span class="sxs-lookup"><span data-stu-id="441f8-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="441f8-106">Формулы в свою очередь, оказывает ссылок на другие ячейки, давая питания для расчета значения в одну ячейку на основе значения другой ячейки.</span><span class="sxs-lookup"><span data-stu-id="441f8-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="441f8-107">При создании или обслуживание сложных фигур, тем не менее, он может быть трудно определить все эти взаимозависимости так как формулы можно ссылаться на любую ячейку в документе, будь то ячеек в одной таблицы свойств фигуры или ячейки, относящегося к другой объект в документе, например страницы, стиль, образец или другую фигуру.</span><span class="sxs-lookup"><span data-stu-id="441f8-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="441f8-108">Окно **Трассировки формул** предоставляет сведения, которые помогут вам понять последствия изменения, внесенные в ячейки.</span><span class="sxs-lookup"><span data-stu-id="441f8-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="441f8-109">Отображение трассировки окно формулы</span><span class="sxs-lookup"><span data-stu-id="441f8-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="441f8-110">Для просмотра окна **Трассировки формул** с окном ShapeSheet active в разделе **Средства фигуры** на ** разработки ** вкладка, группа **Трассировки формул** , выберите **Показать окно**.</span><span class="sxs-lookup"><span data-stu-id="441f8-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the ** Design ** tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="441f8-111">Окно **Трассировки формул** отображается закрепленного окна ShapeSheet по умолчанию, но — привязанного окно, которое может быть прикреплено, отсоединяться и располагаться или объединения с других доступных привязанного таблицы свойств фигуры windows, например окно **Проводника стилей** .</span><span class="sxs-lookup"><span data-stu-id="441f8-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="441f8-112">Зависимые ячейки</span><span class="sxs-lookup"><span data-stu-id="441f8-112">Tracing dependent cells</span></span>

<span data-ttu-id="441f8-113">Чтобы просмотреть список ячеек, зависимых от конкретного ячейки, выберите эту ячейку в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="441f8-113">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window.</span></span> <span data-ttu-id="441f8-114">В этом примере при выборе ячейки ширины.</span><span class="sxs-lookup"><span data-stu-id="441f8-114">In this example, the Width cell is selected.</span></span> 
  
![](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="441f8-115">Чтобы просмотреть его зависимые ячейки в группе **Трассировки формул**, нажмите кнопку **Зависимые**.</span><span class="sxs-lookup"><span data-stu-id="441f8-115">To view its dependent cells, in the **Formula Tracing**group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="441f8-116">В окне **Трассировки формул** появится список всех ячеек ссылки на ячейки ширины.</span><span class="sxs-lookup"><span data-stu-id="441f8-116">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="441f8-117">Можно перейти к любую ячейку в списке, дважды щелкнув его записи в окне **Трассировки формул** .</span><span class="sxs-lookup"><span data-stu-id="441f8-117">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="441f8-118">Precendent ячейки</span><span class="sxs-lookup"><span data-stu-id="441f8-118">Tracing precendent cells</span></span>

<span data-ttu-id="441f8-119">Чтобы просмотреть список ячеек, определенного ячейки зависит от выберите ячейку в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="441f8-119">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window.</span></span> <span data-ttu-id="441f8-120">В этом примере при выборе ячейки Geometry1.X2.</span><span class="sxs-lookup"><span data-stu-id="441f8-120">In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="441f8-121">Чтобы просмотреть его влияющие ячейки в группе **Трассировки формул**, нажмите кнопку **Влияющие**.</span><span class="sxs-lookup"><span data-stu-id="441f8-121">To view its precedent cells, in the **Formula Tracing**group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="441f8-122">Появится список всех ячеек, которые ячейки Geometry1.X2 зависит от в окне **Трассировки формул** .</span><span class="sxs-lookup"><span data-stu-id="441f8-122">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="441f8-123">Можно перейти к любую ячейку в списке, дважды щелкнув его записи в окне **Трассировки формул** .</span><span class="sxs-lookup"><span data-stu-id="441f8-123">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

