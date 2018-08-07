---
title: Строка Ellipse (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Содержит x - и y-координаты центра эллипса и двумя точками на эллипс.
ms.openlocfilehash: 0a2acb0efa20f67d04581f827edbfc4fb4a2d6b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813677"
---
# <a name="ellipse-row-geometry-section"></a>Строка Ellipse (раздел "Геометрия")

Содержит *x* - и *y* -координаты центра эллипса и двумя точками на эллипс. 
  
Строка эллипс содержит следующие ячеек.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -координаты центральной точки.  <br/> |
|[Да](y-cell-geometry-section.md) <br/> |*Y* -координат центральной точки.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |X координата одной точки на эллипс; в сочетании с *y* -координата, представленное B ячейки.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y* -координата одной точки на эллипс; в сочетании с представленной ячейке по оси x.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X* -координаты другой точки на эллипс; в сочетании с *y* -координата, представленного в ячейке D.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |*Y* -координат другой точки на эллипс; в сочетании с *y* -координата, представленный в ячейку C.  <br/> |
   
## <a name="remarks"></a>Замечания

Раздел геометрии содержит эллипсы или строке InfiniteLine не должен содержать других строк.
  

