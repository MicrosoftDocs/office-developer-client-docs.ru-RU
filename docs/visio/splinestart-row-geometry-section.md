---
title: SplineStart Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Содержит координаты x и y для второй контрольной точки сплайна, второй Кнот, ее первый Кнот, последний кнот и степень сплайна.
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358795"
---
# <a name="splinestart-row-geometry-section"></a>SplineStart Row (Geometry Section)

Содержит координаты *x* и *y* для второй контрольной точки сплайна, второй Кнот, ее первый Кнот, последний кнот и степень сплайна. 
  
Строка строка splinestart содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *X* второй контрольной точки сплайна.  <br/> |
|[Y (да)](y-cell-geometry-section.md) <br/> |Координата *Y* второй контрольной точки сплайна.  <br/> |
|[А](a-cell-geometry-section.md) <br/> |Второй кнот сплайна.  <br/> |
|[З](b-cell-geometry-section.md) <br/> |Первый кнот сплайна.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Последний кнот сплайна.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Степень сплайна (целое число от 1 до 25).  <br/> |
   
## <a name="remarks"></a>Примечания

Visio отображает определение сплайна в геометрическом разделе, содержащем строку строка splinestart, за которой следует одна или несколько строк строка splineknot. Строке строка splinestart должен предшествовать другой тип строки, например строка MoveTo, чтобы показать первую контрольную точку сплайна. Предыдущая строка может быть строкой LineTo, строка ArcTo, NURBSTo, полисплайна или строка ellipticalarcto, если сплайн соответствует сегменту этого типа.
  

