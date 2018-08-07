---
title: Строка RelQuadBezTo (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Содержит x - и y - координаты конечной точки кривая Безье относительно фигуры ширину и высоту и x - и y-координаты точки управления фигуры график относительно ширины и высоты.
ms.openlocfilehash: 99796e85a857fd320598cb48993fc29bdfa4964d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814608"
---
# <a name="relquadbezto-row-geometry-section"></a>Строка RelQuadBezTo (раздел "Геометрия")

Содержит *x* - и *y* - координаты конечной точки кривая Безье относительно фигуры ширину и высоту и *x* - и *y* -координаты точки управления фигуры график относительно ширины и высоты. 
  
> [!NOTE]
> Строка **RelQuadBezTo** только могут быть сохранены в форматы файлов vsdx (en), .vsdm, .vstx, .vstm, .vssx и .vssm. При сохранении файла в Visio 2003-2010 форматы строки **RelQuadBezTo** преобразуется в строку [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Строка **RelQuadBezTo** содержит следующие ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -координаты окончания вершины кривая Безье ширине фигуры.  <br/> |
|[Да](y-cell-geometry-section.md) <br/> |*Y* -координат окончания вершины кривая Безье высоте фигуры.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -координата точки управления график ширине фигуры; точка дуги. Контрольная точка расположена лучше всего о пользователю между начала и окончания грани дуги.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y* -координата точки управления график высоте фигуры.  <br/> |
   

