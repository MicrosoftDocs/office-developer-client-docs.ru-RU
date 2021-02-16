---
title: О окне проводника стилей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60119
localization_priority: Normal
ms.assetid: bfdc1a63-c355-c759-bdfa-ce27e3ad10e7
description: Окно проводника стилей предоставляет разработчикам фигур быстрый способ определить, какие ячейки фигур наследуются от заданного стиля, или стиль, от которого данной ячейки наследует ее значение.
ms.openlocfilehash: 55800b692443bae3720b433e5a6178f2709d3675
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431787"
---
# <a name="about-the-style-explorer-window"></a><span data-ttu-id="cb2ac-103">О окне проводника стилей</span><span class="sxs-lookup"><span data-stu-id="cb2ac-103">About the Style Explorer Window</span></span>

<span data-ttu-id="cb2ac-104">Окно **проводника** стилей позволяет разработчикам фигур быстро определить, какие ячейки фигур наследуются от заданного стиля, или стиль, от которого данной ячейки наследует ее значение.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-104">The **Style Explorer** window provides shape developers with a quick way to determine which shape cells inherit from a given style, or the style from which a given cell inherits its value.</span></span> 
  
<span data-ttu-id="cb2ac-105">Стили — это именуемая коллекция атрибутов форматирования, которые можно применить к фигуре.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-105">Styles are named collections of formatting attributes that you can apply to a shape.</span></span> <span data-ttu-id="cb2ac-106">В Microsoft Visio один стиль может определять атрибуты текста, строк и заливки в качестве эффективного способа обеспечения согласованности фигур.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-106">In Microsoft Visio, a single style can define text, line, and fill attributes as an efficient way to ensure consistency in your shapes.</span></span> <span data-ttu-id="cb2ac-107">Кроме того, можно также определить стиль для любого класса атрибута (текст, строка или заливка) или любой комбинации атрибутов.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-107">Additionally, you can also define a style for any one class of attribute (text, line, or fill) or any combination of attributes.</span></span> 
  
<span data-ttu-id="cb2ac-108">В отличие от фигур, к которым вы применили атрибуты форматирования по отдельности, фигуры, которые получают форматирование от стиля, не только обеспечивают согласованность, но и лучше реагируют при их создания, перемещении, масштабирования или повороте.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-108">Unlike shapes to which you've applied formatting attributes individually, shapes that derive their formatting from a style not only ensure consistency but also respond better when they are created, moved, scaled, or rotated.</span></span> 
  
<span data-ttu-id="cb2ac-109">Окно **проводника** стилей предоставляет сведения, необходимые для лучшего понимания последствий изменений, которые вы внося в фигуры.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-109">The **Style Explorer** window provides the information you need to understand better the implications of changes you make to shapes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cb2ac-110">Значения ячеек, которые кажутся черными в окне таблицы фигур, наследуются; те, которые отображаются синим цветом, являются локальными.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-110">Cell values that appear black in the ShapeSheet window are inherited; those that appear blue are local.</span></span> 
  
## <a name="using-the-style-explorer-window"></a><span data-ttu-id="cb2ac-111">Использование окна проводника стилей</span><span class="sxs-lookup"><span data-stu-id="cb2ac-111">Using the Style Explorer window</span></span>

<span data-ttu-id="cb2ac-112">Чтобы **просмотреть** окно проводника стилей с активным окном таблицы фигур, на  вкладке "Конструктор средств **shapeSheet"** в группе "Просмотр" выберите проводник **стилей.**</span><span class="sxs-lookup"><span data-stu-id="cb2ac-112">To view the **Style Explorer** window, with the ShapeSheet window active, on the **ShapeSheet Tools Design** tab, in the **View** group, select **Style Explorer**.</span></span> <span data-ttu-id="cb2ac-113">Окно  проводника стилей по умолчанию закреплено в окне таблицы фигур, но является закрепленным окном, которое можно прикрепить, с  плавающей точкой или объединить с другими доступными закрепленными окнами таблицы фигур, например окном трасситуры формул.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-113">The **Style Explorer** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated, or merged with other available anchored ShapeSheet windows, for example, the **Formula Tracing** window.</span></span> <span data-ttu-id="cb2ac-114">Окно **проводника стилей** содержит древообразное отображение всех стилей, определенных в текущем документе.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-114">The **Style Explorer** window contains a treeview display of all the styles defined in the current drawing.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cb2ac-115">Чтобы получить сведения о стиле, щелкните его  правой кнопкой мыши в окне проводника стилей, чтобы просмотреть его таблицу фигур.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-115">To get information about a style, you can right-click the style in the **Style Explorer** window to view its ShapeSheet.</span></span> 
  
<span data-ttu-id="cb2ac-116">Окно **проводника стилей** предоставляет следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="cb2ac-116">The **Style Explorer** window provides the following information:</span></span> 
  
- <span data-ttu-id="cb2ac-117">Ячейки, наследуемые значения из выбранного стиля. При выборе стиля в  окне проводника стилей все ячейки в окне таблицы фигур, наследуемые от этого стиля, отображаются без сковыва, а ячейки, не наследуемые от этого стиля, отображаются слегка скалярными.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-117">The cells that inherit their values from a selected style.When you select a style in the **Style Explorer** window, all cells in the ShapeSheet window that inherit from that style appear without hatching, while cells that do not inherit from that style appear lightly hatched.</span></span> 
    
- <span data-ttu-id="cb2ac-118">Стиль, от которого выбранная ячейка наследует свое значение. При выборе ячейки ShapeSheet стиль, от которого она наследует свое значение, отображается на панели задач в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="cb2ac-118">The style from which a selected cell inherits its value.When you select a ShapeSheet cell, the style from which it inherits its value is displayed on the taskbar under the ShapeSheet window.</span></span> 
    

