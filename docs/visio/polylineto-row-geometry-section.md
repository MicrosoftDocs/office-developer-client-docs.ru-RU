---
title: PolylineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Содержит координаты x и y последней точки ломаной линии и формулы ломаной линии.
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439466"
---
# <a name="polylineto-row-geometry-section"></a>PolylineTo Row (Geometry Section)

Содержит координаты *x* и *y* последней точки ломаной линии и формулы ломаной линии. 
  
Строка с презначением в виде lineTo содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *X* последней вершины ломаной линии.  <br/> |
|[Y (да)](y-cell-geometry-section.md) <br/> |Координата *Y* последней вершины ломаной линии.  <br/> |
|[Определенно](a-cell-geometry-section.md) <br/> |Формула ломаной линии.  <br/> |
   
## <a name="remarks"></a>Примечания

Линии, представленные в виде строки ломаной линии, эквивалентны строкам, представленным как последовательность строк LineTo, но строка ломаной линии более эффективна. Вы можете изменить строку lineTo на строку LineTo, чтобы можно было легко увидеть геометрию фигуры. Для этого щелкните правой кнопкой мыши строку, а затем выберите **развернуть строку** в контекстном меню. 
  
Чтобы изменить тип строки на строку, щелкните строку правой кнопкой мыши и выберите в контекстном меню команду **изменить тип строки** . 
  

