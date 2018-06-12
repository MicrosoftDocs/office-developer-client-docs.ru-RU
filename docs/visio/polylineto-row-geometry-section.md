---
title: Строка PolylineTo (раздел геометрии)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Содержит x - и y-координаты последнего точки ломаной и ломаной формулы.
ms.openlocfilehash: 56cecb2eeaa1702461b1096fe468974f2f0b1f52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814388"
---
# <a name="polylineto-row-geometry-section"></a>Строка PolylineTo (раздел геометрии)

Содержит *x* - и *y* -координаты последнего точки ломаной и ломаной формулы. 
  
Строка PolylineTo содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -координаты окончания вершины ломаной.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -координат окончания вершины ломаной.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Формула ломаной.  <br/> |
   
## <a name="remarks"></a>Замечания

Строки, представленные в виде строки ломаной эквивалентны на линии, представленные в виде последовательности строк LineTo, но ломаной строке эффективнее. Можно переместить строку PolylineTo LineTo строки, можно легко посмотреть Геометрия фигуры. Для этого щелкните правой кнопкой мыши строку PolylineTo и нажмите кнопку **Развернуть строку** в контекстном меню. 
  
Чтобы изменить тип строки на PolylineTo строку, щелкните правой кнопкой мыши строку и нажмите кнопку **Изменить тип строки** в контекстном меню. 
  

