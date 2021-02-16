---
title: RelLineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Содержит координаты x и y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437163"
---
# <a name="rellineto-row-geometry-section"></a>RelLineTo Row (Geometry Section)

Содержит  *координаты*  x и  *y*  конечной вершины сегмента прямой линии относительно ширины и высоты фигуры. 
  
> [!NOTE]
> Строка **RelLineTo** может сохраняться только в форматах VSDX, VSDM, VSTX, VSTM, VSSX и VSSM. При сохранении файла в форматах Visio 2003-2010 строка **RelLineTo** преобразуется в [строку LineTo.](lineto-row-geometry-section.md) 
  
Строка **RelLineTo** содержит следующие ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |X-координата конечной вершины прямого сегмента относительно ширины фигуры.   <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Координата  *Y*  конечной вершины сегмента прямой линии относительно высоты фигуры.  <br/> |
   
## <a name="remarks"></a>Примечания

Значения в строке **RelLineTo** эквивалентны значениям в строке [LineTo,](lineto-row-geometry-section.md) умноженным на ширину и высоту фигуры. Например, строку **RelLineTo,** где значение ячейки **X** — "0", а значение ячейки **Y** — "0,5", можно заменить строкой **LineTo,** где значение ячейки **X** — это формула "Width 0", а ячейка ***Y***— формула "Height 0.5". 
  

