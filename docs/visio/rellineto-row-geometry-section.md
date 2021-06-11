---
title: RelLineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Содержит x и y-координаты конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437163"
---
# <a name="rellineto-row-geometry-section"></a>RelLineTo Row (Geometry Section)

Содержит  *x*  и  *y-координаты*  конечной вершины сегмента прямой линии относительно ширины и высоты фигуры. 
  
> [!NOTE]
> Строка **RelLineTo** может сохраняться только в форматах файлов .vsdx, .vsdm, vstx, .vstm, .vssx и .vssm. Если файл сохранен в форматах 2003-2010 Visio, строка **RelLineTo** преобразуется в строку [LineTo.](lineto-row-geometry-section.md) 
  
Строка **RelLineTo** содержит следующие ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |X-координата конечной вершины сегмента прямой линии относительно ширины фигуры.   <br/> |
|[Да](y-cell-geometry-section.md) <br/> |Y-координата конечной вершины сегмента прямой линии относительно высоты фигуры.   <br/> |
   
## <a name="remarks"></a>Примечания

Значения в строке **RelLineTo** эквивалентны значениям в строке [LineTo,](lineto-row-geometry-section.md) умножаемой на ширину и высоту фигуры. Например: строка **RelLineTo,** где  значение X-ячейки — "0", а ячейка **Y** — "0.5", может быть заменена строкой **LineTo,** где значение ячейки **X** — формула "Ширина *0", а **ячейка Y***— формула "Высота 0.5". 
  

