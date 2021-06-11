---
title: Ellipse Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Содержит x и y-координаты центральной точки эллипса и две точки на эллипсе.
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421832"
---
# <a name="ellipse-row-geometry-section"></a>Ellipse Row (Geometry Section)

Содержит  *x*  и  *y-координаты*  центральной точки эллипса и две точки на эллипсе. 
  
Строка Ellipse содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |X-координата центральной точки.   <br/> |
|[Да](y-cell-geometry-section.md) <br/> |*Y-координата* центральной точки.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |X-координата одной точки на эллипсе; в паре  *с y-coordinate,*  представленным ячейкой B.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*y-координата* одной точки на эллипсе; в паре с X-координатами, представленными ячейкой A.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X-координата* другой точки на эллипсе; в паре *с y-координатами,* представленными ячейкой D.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |*y-координата* другой точки на эллипсе; в паре *с y-coordinate,* представленным ячейкой C.  <br/> |
   
## <a name="remarks"></a>Примечания

Раздел геометрии, содержащий строку Ellipse или InfiniteLine, не должен содержать другие строки.
  

