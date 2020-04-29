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
description: Содержит координаты x и y, а также арксинус круга.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430044"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="3438a-103">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="3438a-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="3438a-104">Содержит координаты *x* и *y* , а также арксинус круга.</span><span class="sxs-lookup"><span data-stu-id="3438a-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="3438a-105">Строка строка ArcTo содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="3438a-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="3438a-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3438a-106">**Cell**</span></span>|<span data-ttu-id="3438a-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3438a-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3438a-108">X</span><span class="sxs-lookup"><span data-stu-id="3438a-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="3438a-109">Координата *X* последней вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="3438a-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="3438a-110">Y (да)</span><span class="sxs-lookup"><span data-stu-id="3438a-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="3438a-111">Координата *Y* последней вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="3438a-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="3438a-112">Определенно</span><span class="sxs-lookup"><span data-stu-id="3438a-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="3438a-113">Расстояние от средней дуги до средней точки аккорда.</span><span class="sxs-lookup"><span data-stu-id="3438a-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3438a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3438a-114">Remarks</span></span>

<span data-ttu-id="3438a-115">Дуги, рисуемые в Visio, являются эллиптическими дугами, даже если они основаны на круге.</span><span class="sxs-lookup"><span data-stu-id="3438a-115">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle.</span></span> <span data-ttu-id="3438a-116">По умолчанию отображаемые дуги представлены в виде строки строка ellipticalarcto в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="3438a-116">By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window.</span></span> <span data-ttu-id="3438a-117">Чтобы отобразить строку строка ArcTo в окне таблицы свойств фигуры, необходимо нарисовать дугу и затем изменить тип строки строка ellipticalarcto на тип строки строка ArcTo; в результате вы изменяете дугу эллиптического кружка на круговую дугу.</span><span class="sxs-lookup"><span data-stu-id="3438a-117">To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="3438a-118">Чтобы изменить тип строки, щелкните строку правой кнопкой мыши и выберите в контекстном меню команду **изменить тип строки** .</span><span class="sxs-lookup"><span data-stu-id="3438a-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

