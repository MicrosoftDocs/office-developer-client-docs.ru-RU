---
title: Строка RelLineTo (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Содержит x - и y-координаты окончания вершины отрезка прямой линии относительно ширины и высоты фигуры.
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814564"
---
# <a name="rellineto-row-geometry-section"></a>Строка RelLineTo (раздел "Геометрия")

Содержит *x* - и *y* -координаты окончания вершины отрезка прямой линии относительно ширины и высоты фигуры. 
  
> [!NOTE]
> Строка **RelLineTo** только могут быть сохранены в форматы файлов vsdx (en), .vsdm, .vstx, .vstm, .vssx и .vssm. При сохранении файла в Visio 2003-2010 форматы строки **RelLineTo** преобразуется в строку [LineTo](lineto-row-geometry-section.md) . 
  
Строка **RelLineTo** содержит следующие ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -координаты окончания вершины сегмента прямой ширине фигуры.  <br/> |
|[Да](y-cell-geometry-section.md) <br/> |*Y* -координат окончания вершины сегмента прямой высоте фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Значения в строке **RelLineTo** эквивалентны значения в строку [LineTo](lineto-row-geometry-section.md) , умноженное ширину и высоту фигуры. Например: **RelLineTo** строку, где значение ячейки **X** — «0» и «0,5» имеет значение ячейки **Y** можно заменить **LineTo** строку, где значение ячейки **X** — это формула «ширина*0" и ячейки **Y** — это Формула «Высота*0,5.» 
  

