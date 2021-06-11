---
title: О окне Обозреватель стиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60119
localization_priority: Normal
ms.assetid: bfdc1a63-c355-c759-bdfa-ce27e3ad10e7
description: Окно Обозреватель стиля позволяет разработчикам фигур быстро определить, какие ячейки фигур наследуют из заданного стиля или стиль, из которого данной ячейке наследуется ее значение.
ms.openlocfilehash: 55800b692443bae3720b433e5a6178f2709d3675
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431787"
---
# <a name="about-the-style-explorer-window"></a><span data-ttu-id="54d2d-103">О окне Обозреватель стиля</span><span class="sxs-lookup"><span data-stu-id="54d2d-103">About the Style Explorer Window</span></span>

<span data-ttu-id="54d2d-104">Окно **Обозреватель** стиля позволяет разработчикам фигур быстро определить, какие ячейки фигур наследуют из заданного стиля или стиль, из которого данной ячейке наследуется ее значение.</span><span class="sxs-lookup"><span data-stu-id="54d2d-104">The **Style Explorer** window provides shape developers with a quick way to determine which shape cells inherit from a given style, or the style from which a given cell inherits its value.</span></span> 
  
<span data-ttu-id="54d2d-105">Стили называются коллекциями атрибутов форматирования, которые можно применить к фигуре.</span><span class="sxs-lookup"><span data-stu-id="54d2d-105">Styles are named collections of formatting attributes that you can apply to a shape.</span></span> <span data-ttu-id="54d2d-106">В microsoft Visio один стиль может определять атрибуты текста, строки и заполнять их как эффективный способ обеспечения согласованности фигур.</span><span class="sxs-lookup"><span data-stu-id="54d2d-106">In Microsoft Visio, a single style can define text, line, and fill attributes as an efficient way to ensure consistency in your shapes.</span></span> <span data-ttu-id="54d2d-107">Кроме того, можно также определить стиль для любого класса атрибута (текст, строка или заливка) или любого сочетания атрибутов.</span><span class="sxs-lookup"><span data-stu-id="54d2d-107">Additionally, you can also define a style for any one class of attribute (text, line, or fill) or any combination of attributes.</span></span> 
  
<span data-ttu-id="54d2d-108">В отличие от фигур, к которым вы применяли атрибуты форматирования по отдельности, фигуры, которые получают форматирование из стиля, не только обеспечивают согласованность, но и лучше реагируют при их создания, перемещении, масштабе или повороте.</span><span class="sxs-lookup"><span data-stu-id="54d2d-108">Unlike shapes to which you've applied formatting attributes individually, shapes that derive their formatting from a style not only ensure consistency but also respond better when they are created, moved, scaled, or rotated.</span></span> 
  
<span data-ttu-id="54d2d-109">Окно **Обозреватель стиля** предоставляет сведения, необходимые для лучшего понимания последствий изменений, внесенных в формы.</span><span class="sxs-lookup"><span data-stu-id="54d2d-109">The **Style Explorer** window provides the information you need to understand better the implications of changes you make to shapes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="54d2d-110">Наследуются значения ячейки, которые кажутся черными в окне ShapeSheet; те, которые отображаются синими, являются локальными.</span><span class="sxs-lookup"><span data-stu-id="54d2d-110">Cell values that appear black in the ShapeSheet window are inherited; those that appear blue are local.</span></span> 
  
## <a name="using-the-style-explorer-window"></a><span data-ttu-id="54d2d-111">Использование окна Обозреватель стилей</span><span class="sxs-lookup"><span data-stu-id="54d2d-111">Using the Style Explorer window</span></span>

<span data-ttu-id="54d2d-112">Чтобы просмотреть окно **Обозреватель** стилей с активным окном ShapeSheet, на вкладке **ShapeSheet Tools Design** в группе **View** выберите **Обозреватель стиля**.</span><span class="sxs-lookup"><span data-stu-id="54d2d-112">To view the **Style Explorer** window, with the ShapeSheet window active, on the **ShapeSheet Tools Design** tab, in the **View** group, select **Style Explorer**.</span></span> <span data-ttu-id="54d2d-113">Окно **Обозреватель** стиля по умолчанию состыковано в окне ShapeSheet, но является якорным окном, которое можно пристыковать, поплыть или объединить с другими доступными закрепленными окнами ShapeSheet, например окном трассивки **Формулы.**</span><span class="sxs-lookup"><span data-stu-id="54d2d-113">The **Style Explorer** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated, or merged with other available anchored ShapeSheet windows, for example, the **Formula Tracing** window.</span></span> <span data-ttu-id="54d2d-114">Окно **Обозреватель** стиля содержит отображение treeview всех стилей, определенных в текущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="54d2d-114">The **Style Explorer** window contains a treeview display of all the styles defined in the current drawing.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="54d2d-115">Чтобы получить сведения о стиле, вы можете щелкнуть правой кнопкой мыши стиль в окне **Обозреватель** стиля, чтобы просмотреть его таблицу ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="54d2d-115">To get information about a style, you can right-click the style in the **Style Explorer** window to view its ShapeSheet.</span></span> 
  
<span data-ttu-id="54d2d-116">В **окне Обозреватель** стилей содержится следующая информация:</span><span class="sxs-lookup"><span data-stu-id="54d2d-116">The **Style Explorer** window provides the following information:</span></span> 
  
- <span data-ttu-id="54d2d-117">Ячейки, наследуя свои значения из выбранного стиля. При выборе стиля в окне **Style Explorer** все ячейки в окне ShapeSheet, унаследованные от этого стиля, отображаются без штриховки, а ячейки, которые не наследуют этот стиль, выглядят легко вылупившись.</span><span class="sxs-lookup"><span data-stu-id="54d2d-117">The cells that inherit their values from a selected style.When you select a style in the **Style Explorer** window, all cells in the ShapeSheet window that inherit from that style appear without hatching, while cells that do not inherit from that style appear lightly hatched.</span></span> 
    
- <span data-ttu-id="54d2d-118">Стиль, из которого выбранная ячейка наследует свое значение. При выборе ячейки ShapeSheet на панели задач в окне ShapeSheet отображается стиль, от которого она наследует свое значение.</span><span class="sxs-lookup"><span data-stu-id="54d2d-118">The style from which a selected cell inherits its value.When you select a ShapeSheet cell, the style from which it inherits its value is displayed on the taskbar under the ShapeSheet window.</span></span> 
    

