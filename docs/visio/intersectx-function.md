---
title: Функция INTERSECTX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
localization_priority: Normal
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: Возвращает x-координату (в локальной системе координат) точки, в которой пересекаются две линии.
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418276"
---
# <a name="intersectx-function"></a>Функция INTERSECTX

Возвращает  *x-координату*  (в локальной системе координат) точки, в которой пересекаются две линии. 
  
## <a name="syntax"></a>Синтаксис

INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Обязательна  <br/> |**Number** <br/> |X-координата точки в первой строке.   <br/> |
| _y1_ <br/> |Обязательна  <br/> |**Number** <br/> |Y-координата точки в первой строке.   <br/> |
| _angle1_ <br/> |Обязательна  <br/> |**Number** <br/> | Значение ячейки Angle для первой строки.  <br/> |
| _x2_ <br/> |Обязательна  <br/> |**Number** <br/> |X-координата точки во второй строке.   <br/> |
| _y2_ <br/> |Обязательна  <br/> |**Number** <br/> |Y-координата точки во второй строке.   <br/> |
| _angle2_ <br/> |Обязательна  <br/> |**Number** <br/> |Значение ячейки Angle для второй строки.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Числовой
  
## <a name="remarks"></a>Примечания

Каждая строка определяется как точка *(x,y)* и угол. 
  
Microsoft Visio использует эту функцию в ячейке PinX фигуры, привязаемой к повернутой направляющей. 
  
Если линии не пересекаются, функция возвращает ошибку деления на ноль (#DIV/0!), которую Visio игнорирует, восстанавливая последнее известное значение точки. 
  
## <a name="example"></a>Пример

INTERSECTX(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide! PinX,HorzGuide! PinY,HorzGuide! Angle) 
  
Возвращает  *x-координату*  точки пересечения VertGuide и HorzGuide в единицах страницы. 
  

