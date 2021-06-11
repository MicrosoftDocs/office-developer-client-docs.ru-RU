---
title: ArcTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Содержит x и y-координаты и носовую часть круговой дуги.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430044"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="10bef-103">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="10bef-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="10bef-104">Содержит  *x*  и  *y-координаты*  и носовую часть круговой дуги.</span><span class="sxs-lookup"><span data-stu-id="10bef-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="10bef-105">Строка ArcTo содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="10bef-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="10bef-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="10bef-106">**Cell**</span></span>|<span data-ttu-id="10bef-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="10bef-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10bef-108">X</span><span class="sxs-lookup"><span data-stu-id="10bef-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="10bef-109">Координата *X* последней вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="10bef-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="10bef-110">Да</span><span class="sxs-lookup"><span data-stu-id="10bef-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="10bef-111">Координата *Y* последней вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="10bef-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="10bef-112">A</span><span class="sxs-lookup"><span data-stu-id="10bef-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="10bef-113">Расстояние от середины дуги до середины аккорда.</span><span class="sxs-lookup"><span data-stu-id="10bef-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10bef-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="10bef-114">Remarks</span></span>

<span data-ttu-id="10bef-115">Дуги, нарисованные Visio, являются эллиптичными дугами, даже если они основаны на круге.</span><span class="sxs-lookup"><span data-stu-id="10bef-115">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle.</span></span> <span data-ttu-id="10bef-116">По умолчанию нарисованные дуги представляются строкой EllipticalArcTo в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="10bef-116">By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window.</span></span> <span data-ttu-id="10bef-117">Чтобы показать строку ArcTo в окне ShapeSheet, необходимо нарисовать дугу, а затем изменить тип строки EllipticalArcTo на тип строки ArcTo; фактически вы меняете эллиптическую дугу на круговую.</span><span class="sxs-lookup"><span data-stu-id="10bef-117">To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="10bef-118">Чтобы изменить тип строки, щелкните правой кнопкой мыши строку и нажмите **кнопку Изменить** строку в меню ярлыка.</span><span class="sxs-lookup"><span data-stu-id="10bef-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

