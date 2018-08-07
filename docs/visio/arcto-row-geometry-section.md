---
title: Строка ArcTo (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Содержит x - и y-координаты и галстук дугу.
ms.openlocfilehash: 77ed0dcaee7ddefa8771d3e890776d4adfcc3b40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813159"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="3d23e-103">Строка ArcTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="3d23e-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="3d23e-104">Содержит *x* - и *y* -координаты и галстук дугу.</span><span class="sxs-lookup"><span data-stu-id="3d23e-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="3d23e-105">Строка ArcTo содержит следующие ячеек.</span><span class="sxs-lookup"><span data-stu-id="3d23e-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="3d23e-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3d23e-106">**Cell**</span></span>|<span data-ttu-id="3d23e-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3d23e-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d23e-108">X</span><span class="sxs-lookup"><span data-stu-id="3d23e-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="3d23e-109">*X* -координаты окончания вершины дугу.</span><span class="sxs-lookup"><span data-stu-id="3d23e-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="3d23e-110">Да</span><span class="sxs-lookup"><span data-stu-id="3d23e-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="3d23e-111">*Y* -координат окончания вершины дугу.</span><span class="sxs-lookup"><span data-stu-id="3d23e-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="3d23e-112">A</span><span class="sxs-lookup"><span data-stu-id="3d23e-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="3d23e-113">Расстояние от среднего дуги по центру его кабеля.</span><span class="sxs-lookup"><span data-stu-id="3d23e-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d23e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3d23e-114">Remarks</span></span>

<span data-ttu-id="3d23e-115">Дуг в Visio, эллиптических дуг даже в том случае, если они будут основываться круг.</span><span class="sxs-lookup"><span data-stu-id="3d23e-115">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle.</span></span> <span data-ttu-id="3d23e-116">По умолчанию отображаемого дуг представлены в виде строки EllipticalArcTo в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="3d23e-116">By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window.</span></span> <span data-ttu-id="3d23e-117">Чтобы показать строку ArcTo в окне таблицы свойств фигуры, необходимо нарисовать дугу и измените тип строки EllipticalArcTo в строку тип ArcTo; фактически переходе руководство дугу.</span><span class="sxs-lookup"><span data-stu-id="3d23e-117">To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="3d23e-118">Чтобы изменить тип строки, щелкните правой кнопкой мыши строку и нажмите кнопку **Изменить тип строки** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="3d23e-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

