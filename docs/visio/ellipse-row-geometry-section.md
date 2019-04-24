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
description: Содержит координаты x и y центральной точки эллипса и две точки эллипса.
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345684"
---
# <a name="ellipse-row-geometry-section"></a>Ellipse Row (Geometry Section)

Содержит координаты *x* и *y* центральной точки эллипса и две точки эллипса. 
  
Строка эллипса содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *x* центральной точки.  <br/> |
|[Y (да)](y-cell-geometry-section.md) <br/> |Координата *y* центральной точки.  <br/> |
|[А](a-cell-geometry-section.md) <br/> |Координата x одной точки эллипса; Связывание с координатой *y* , представленной в ячейке B.  <br/> |
|[З](b-cell-geometry-section.md) <br/> |Координата *y* одной точки эллипса; Связывание с координатой x, представленной ячейкой.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Координата *x* другой точки эллипса; Связывание с координатой *y* , представленной ячейкой D.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Координата *y* другой точки эллипса; Связывание с координатой *y* , представленной в ячейке C.  <br/> |
   
## <a name="remarks"></a>Комментарии

Раздел геометрии, содержащий эллипс или строку строка infiniteline, не должен содержать других строк.
  

