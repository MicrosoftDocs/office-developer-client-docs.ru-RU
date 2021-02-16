---
title: ArcTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Содержит координаты x и y и лук цикловой дуги.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430044"
---
# <a name="arcto-row-geometry-section"></a>ArcTo Row (Geometry Section)

Содержит  *координаты x*  и  *y*  и лук цикловой дуги. 
  
Строка ArcTo содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *X* последней вершины дуги.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Координата *Y* последней вершины дуги.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Расстояние от средней точки дуги до средней точки ее разоряемой.  <br/> |
   
## <a name="remarks"></a>Примечания

Arcs drawn in Visio are elliptical arcs, even if they are based on a circle. По умолчанию нарисованные дуги представлены строкой EllipticalArcTo в окне ShapeSheet. Чтобы отобразить строку ArcTo в окне ShapeSheet, необходимо нарисовать дугу, а затем изменить тип строки EllipticalArcTo на тип строки ArcTo; фактически вы изменяете дугу эллиптических на циклическую.
  
Чтобы изменить тип строки, щелкните ее правой кнопкой мыши и выберите пункт **"Изменить** тип строки" в ярлыковом меню. 
  

