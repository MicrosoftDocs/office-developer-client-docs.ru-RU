---
title: Строка RelCubBezTo (раздел геометрии)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Содержит x - и y - координаты конечной точки кубические Безье график относительно фигуры ширину и высоту, x - и y - координат контрольной точки в начало фигуры график относительно ширины и высоты и x - и y-координаты элемент управления l точка конца фигуры график относительно ширины и высоты.
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814560"
---
# <a name="relcubbezto-row-geometry-section"></a>Строка RelCubBezTo (раздел геометрии)

Содержит *x* - и *y* - координаты конечной точки кубические Безье график относительно фигуры ширину и высоту, *x* - и *y* -координат контрольной точки в начало ширину и высоту фигуры относительно график и *x* - и *y* -координаты точки управления завершения фигуры график относительно ширины и высоты. 
  
> [!NOTE]
> Строка **RelCubBezTo** только могут быть сохранены в форматы файлов vsdx (en), .vsdm, .vstx, .vstm, .vssx и .vssm. При сохранении файла в Visio 2003-2010 форматы строки **RelCubBezTo** преобразуется в строку [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Строка **RelCubBezTo** содержит следующие ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -координаты окончания вершины кубические Безье график ширине фигуры.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -координат окончания вершины кубические Безье график высоте фигуры.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -координата график абонента Приступая к работе с контрольной точки относительно ширины фигуры; точка дуги. Контрольная точка лучше всего находится между начала и окончания грани дуги.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y* -координата график абонента Приступая к работе с контрольной точки высоте фигуры.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X* -координата график окончания точки управления ширине фигуры; точка дуги. Контрольная точка лучше всего находится между первый элемент управления точка и заканчивая грани дуги.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |*Y* -координата график окончания точки управления высоте фигуры.  <br/> |
   
