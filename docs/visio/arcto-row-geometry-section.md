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
description: Содержит координаты x и y, а также арксинус круга.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430044"
---
# <a name="arcto-row-geometry-section"></a>ArcTo Row (Geometry Section)

Содержит координаты *x* и *y* , а также арксинус круга. 
  
Строка строка ArcTo содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *X* последней вершины дуги.  <br/> |
|[Y (да)](y-cell-geometry-section.md) <br/> |Координата *Y* последней вершины дуги.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Расстояние от средней дуги до средней точки аккорда.  <br/> |
   
## <a name="remarks"></a>Примечания

Дуги, рисуемые в Visio, являются эллиптическими дугами, даже если они основаны на круге. По умолчанию отображаемые дуги представлены в виде строки строка ellipticalarcto в окне таблицы свойств фигуры. Чтобы отобразить строку строка ArcTo в окне таблицы свойств фигуры, необходимо нарисовать дугу и затем изменить тип строки строка ellipticalarcto на тип строки строка ArcTo; в результате вы изменяете дугу эллиптического кружка на круговую дугу.
  
Чтобы изменить тип строки, щелкните строку правой кнопкой мыши и выберите в контекстном меню команду **изменить тип строки** . 
  

