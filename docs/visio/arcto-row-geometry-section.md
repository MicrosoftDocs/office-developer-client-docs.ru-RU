---
title: Строка ArcTo (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Содержит x - и y-координаты и галстук дугу.
ms.openlocfilehash: 77ed0dcaee7ddefa8771d3e890776d4adfcc3b40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813159"
---
# <a name="arcto-row-geometry-section"></a>Строка ArcTo (раздел "Геометрия")

Содержит *x* - и *y* -координаты и галстук дугу. 
  
Строка ArcTo содержит следующие ячеек.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -координаты окончания вершины дугу.  <br/> |
|[Да](y-cell-geometry-section.md) <br/> |*Y* -координат окончания вершины дугу.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Расстояние от среднего дуги по центру его кабеля.  <br/> |
   
## <a name="remarks"></a>Замечания

Дуг в Visio, эллиптических дуг даже в том случае, если они будут основываться круг. По умолчанию отображаемого дуг представлены в виде строки EllipticalArcTo в окне таблицы свойств фигуры. Чтобы показать строку ArcTo в окне таблицы свойств фигуры, необходимо нарисовать дугу и измените тип строки EllipticalArcTo в строку тип ArcTo; фактически переходе руководство дугу.
  
Чтобы изменить тип строки, щелкните правой кнопкой мыши строку и нажмите кнопку **Изменить тип строки** в контекстном меню. 
  

