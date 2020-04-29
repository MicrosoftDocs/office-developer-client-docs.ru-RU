---
title: Сведения о окне "Обозреватель стилей"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60119
localization_priority: Normal
ms.assetid: bfdc1a63-c355-c759-bdfa-ce27e3ad10e7
description: Окно проводника стилей предоставляет разработчикам фигур быстрый способ определения того, какие ячейки фигуры наследуются от определенного стиля, или стиль, из которого данная ячейка наследует значение.
ms.openlocfilehash: 55800b692443bae3720b433e5a6178f2709d3675
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431787"
---
# <a name="about-the-style-explorer-window"></a><span data-ttu-id="5263a-103">Сведения о окне "Обозреватель стилей"</span><span class="sxs-lookup"><span data-stu-id="5263a-103">About the Style Explorer Window</span></span>

<span data-ttu-id="5263a-104">Окно **проводника стилей** предоставляет разработчикам фигур быстрый способ определения того, какие ячейки фигуры наследуются от определенного стиля, или стиль, из которого данная ячейка наследует значение.</span><span class="sxs-lookup"><span data-stu-id="5263a-104">The **Style Explorer** window provides shape developers with a quick way to determine which shape cells inherit from a given style, or the style from which a given cell inherits its value.</span></span> 
  
<span data-ttu-id="5263a-105">Styles — это именованные коллекции атрибутов форматирования, которые можно применить к фигуре.</span><span class="sxs-lookup"><span data-stu-id="5263a-105">Styles are named collections of formatting attributes that you can apply to a shape.</span></span> <span data-ttu-id="5263a-106">В Microsoft Visio один стиль может определять атрибуты Text, Line и Fill как эффективный способ обеспечения согласованности фигур.</span><span class="sxs-lookup"><span data-stu-id="5263a-106">In Microsoft Visio, a single style can define text, line, and fill attributes as an efficient way to ensure consistency in your shapes.</span></span> <span data-ttu-id="5263a-107">Кроме того, можно определить стиль для любого класса атрибута (Text, Line или Fill) или любой комбинации атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5263a-107">Additionally, you can also define a style for any one class of attribute (text, line, or fill) or any combination of attributes.</span></span> 
  
<span data-ttu-id="5263a-108">В отличие от фигур, к которым вы применили атрибуты форматирования по отдельности, фигуры, которые производят форматирование из стиля, не только обеспечивают согласованность, но и лучше реагируют при создании, перемещении, масштабировании или повороте.</span><span class="sxs-lookup"><span data-stu-id="5263a-108">Unlike shapes to which you've applied formatting attributes individually, shapes that derive their formatting from a style not only ensure consistency but also respond better when they are created, moved, scaled, or rotated.</span></span> 
  
<span data-ttu-id="5263a-109">Окно " **Обозреватель стилей** " предоставляет сведения, необходимые для улучшения влияния изменений, внесенных в фигуры.</span><span class="sxs-lookup"><span data-stu-id="5263a-109">The **Style Explorer** window provides the information you need to understand better the implications of changes you make to shapes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5263a-110">Значения ячеек, которые отображаются черным цветом в окне таблицы свойств фигуры, наследуются; синие должны быть локальными.</span><span class="sxs-lookup"><span data-stu-id="5263a-110">Cell values that appear black in the ShapeSheet window are inherited; those that appear blue are local.</span></span> 
  
## <a name="using-the-style-explorer-window"></a><span data-ttu-id="5263a-111">Использование окна "Обозреватель стилей"</span><span class="sxs-lookup"><span data-stu-id="5263a-111">Using the Style Explorer window</span></span>

<span data-ttu-id="5263a-112">Чтобы открыть окно " **Обозреватель стилей** " с активной страницей таблицы свойств фигуры, на вкладке " **Конструктор" инструментов "Таблица** ", в группе " **представление** " выберите элемент " **Обозреватель стилей**".</span><span class="sxs-lookup"><span data-stu-id="5263a-112">To view the **Style Explorer** window, with the ShapeSheet window active, on the **ShapeSheet Tools Design** tab, in the **View** group, select **Style Explorer**.</span></span> <span data-ttu-id="5263a-113">Окно " **Обозреватель стилей** " по умолчанию отображается в окне таблицы свойств фигуры, но является закрепленным окном, которое можно прикрепить, поплавающее или объединить с другими доступными закрепленными окнами таблицы свойств фигуры, например, окно **трассировки формул** .</span><span class="sxs-lookup"><span data-stu-id="5263a-113">The **Style Explorer** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated, or merged with other available anchored ShapeSheet windows, for example, the **Formula Tracing** window.</span></span> <span data-ttu-id="5263a-114">Окно " **Обозреватель стилей** " содержит отображение всех стилей, определенных в текущем документе TreeView.</span><span class="sxs-lookup"><span data-stu-id="5263a-114">The **Style Explorer** window contains a treeview display of all the styles defined in the current drawing.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5263a-115">Чтобы получить сведения о стиле, можно щелкнуть правой кнопкой мыши стиль в окне " **Обозреватель стилей** ", чтобы просмотреть ее таблицу свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="5263a-115">To get information about a style, you can right-click the style in the **Style Explorer** window to view its ShapeSheet.</span></span> 
  
<span data-ttu-id="5263a-116">Окно " **Обозреватель стилей** " предоставляет следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="5263a-116">The **Style Explorer** window provides the following information:</span></span> 
  
- <span data-ttu-id="5263a-117">Ячейки, которые наследуют их значения из выбранного стиля. При выборе стиля в окне " **Обозреватель стилей** " все ячейки в окне таблицы свойств фигуры, которые наследуются от этого стиля, отображаются без штриховки, а в ячейках, которые не наследуются от этого стиля, отображаются неплотные штрихи.</span><span class="sxs-lookup"><span data-stu-id="5263a-117">The cells that inherit their values from a selected style.When you select a style in the **Style Explorer** window, all cells in the ShapeSheet window that inherit from that style appear without hatching, while cells that do not inherit from that style appear lightly hatched.</span></span> 
    
- <span data-ttu-id="5263a-118">Стиль, в котором выбранная ячейка наследует значение. Когда вы выбираете ячейку таблицы свойств фигуры, стиль, на основе которого он наследует свое значение, отображается на панели задач в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="5263a-118">The style from which a selected cell inherits its value.When you select a ShapeSheet cell, the style from which it inherits its value is displayed on the taskbar under the ShapeSheet window.</span></span> 
    

