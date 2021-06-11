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
description: Возвращает x-coordinate (в локальной системе координат) точки, в которой пересекаются две линии.
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418276"
---
# <a name="intersectx-function"></a>Функция INTERSECTX

Возвращает  *x-coordinate*  (в локальной системе координат) точки, в которой пересекаются две линии. 
  
## <a name="syntax"></a>Синтаксис

INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Обязательный  <br/> |**Number** <br/> |X-координата точки на первой строке.   <br/> |
| _y1_ <br/> |Обязательный  <br/> |**Number** <br/> |Y-координата точки на первой строке.   <br/> |
| _angle1_ <br/> |Обязательный  <br/> |**Number** <br/> | Значение ячейки Angle для первой строки.  <br/> |
| _x2_ <br/> |Обязательный  <br/> |**Number** <br/> |X-координата точки на второй строке.   <br/> |
| _y2_ <br/> |Обязательный  <br/> |**Number** <br/> |Y-координата точки на второй строке.   <br/> |
| _angle2_ <br/> |Обязательный  <br/> |**Number** <br/> |Значение ячейки Angle для второй строки.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Номер
  
## <a name="remarks"></a>Примечания

Каждая строка определяется как точка *(x,y) и* угол. 
  
Microsoft Visio использует эту функцию в ячейке PinX формы, приклеенной к вращаемой направляющей. 
  
Если линии не пересекаются, функция возвращает ошибку разделять на ноль (#DIV/0!), которую Visio игнорирует, восстанавливая последнее известное значение для точки. 
  
## <a name="example"></a>Пример

INTERSECTX(VertGuide! PinX,VertGuide! Piny,VertGuide! Угол, HorzGuide! PinX,HorzGuide! PinY,HorzGuide! Угол) 
  
Возвращает  *x-координату*  точки пересечения VertGuide и HorzGuide в единицах страниц. 
  

