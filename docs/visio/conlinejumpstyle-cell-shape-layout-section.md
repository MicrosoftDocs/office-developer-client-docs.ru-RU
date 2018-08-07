---
title: Ячейка ConLineJumpStyle (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
localization_priority: Normal
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: Определяет стиль значка для строки пересечения динамической соединительной линии.
ms.openlocfilehash: d3e27ddb6689fb5635674b3c4a8462fe587bce7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813471"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>Ячейка ConLineJumpStyle (раздел "Макет фигуры")

Определяет стиль значка для строки пересечения динамической соединительной линии.
  
|**Значение**|**Линии началу работы**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Страница по умолчанию  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |ARC  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Разрывов  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Квадратный  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |Треугольник  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |три стороны  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 сторон  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 сторон  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 сторон  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 сторон  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>Замечания

Можно также значение ячейки с выбор динамического соединителя, нажав кнопку **поведение** группы **Разработки фигуры** на вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " и затем выбрав вкладку **соединителя** . 
  
Чтобы получить ссылку на ячейку ConLineJumpStyle по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ConLineJumpStyle  <br/> |
   
Для получения ссылки на ячейки ConLineJumpStyle по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  

