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
description: Содержит x и y-координаты и носовую часть круговой дуги.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430044"
---
# <a name="arcto-row-geometry-section"></a>ArcTo Row (Geometry Section)

Содержит  *x*  и  *y-координаты*  и носовую часть круговой дуги. 
  
Строка ArcTo содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *X* последней вершины дуги.  <br/> |
|[Да](y-cell-geometry-section.md) <br/> |Координата *Y* последней вершины дуги.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Расстояние от середины дуги до середины аккорда.  <br/> |
   
## <a name="remarks"></a>Примечания

Дуги, нарисованные Visio, являются эллиптичными дугами, даже если они основаны на круге. По умолчанию нарисованные дуги представляются строкой EllipticalArcTo в окне ShapeSheet. Чтобы показать строку ArcTo в окне ShapeSheet, необходимо нарисовать дугу, а затем изменить тип строки EllipticalArcTo на тип строки ArcTo; фактически вы меняете эллиптическую дугу на круговую.
  
Чтобы изменить тип строки, щелкните правой кнопкой мыши строку и нажмите **кнопку Изменить** строку в меню ярлыка. 
  

