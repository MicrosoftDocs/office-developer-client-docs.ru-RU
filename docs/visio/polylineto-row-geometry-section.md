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
description: Содержит x и y-координаты последней точки полилиновой и полилиновой формулы.
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439466"
---
# <a name="polylineto-row-geometry-section"></a>PolylineTo Row (Geometry Section)

Содержит  *x*  и  *y-координаты*  последней точки полилиновой и полилиновой формулы. 
  
Строка PolylineTo содержит следующие ячейки.
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Координата *X* последней вершины ломаной линии.  <br/> |
|[Да](y-cell-geometry-section.md) <br/> |Координата *Y* последней вершины ломаной линии.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Формула полилинов.  <br/> |
   
## <a name="remarks"></a>Примечания

Строки, представленные в качестве строки Polyline, эквивалентны строкам, представленным в качестве последовательности строк LineTo, но строка Polyline эффективнее. Вы можете изменить строку PolylineTo на строку LineTo, чтобы можно было легко увидеть геометрию фигуры. Чтобы сделать это, щелкните правой кнопкой мыши строку PolylineTo, а затем щелкните **Расширение строки** в меню ярлыка. 
  
Чтобы изменить тип строки на строку PolylineTo, щелкните правой кнопкой мыши строку и нажмите кнопку **Изменить** тип строки в меню ярлыка. 
  

