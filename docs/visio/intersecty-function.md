---
title: Функция INTERSECTY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Возвращает y-координата (в локальной системе координат) точки пересечения двух линий.
ms.openlocfilehash: c3c0e9afef317ed4c647f1d236c4c3a29c6cdaa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813968"
---
# <a name="intersecty-function"></a>Функция INTERSECTY

Возвращает *y* -координата (в локальной системе координат) точки пересечения двух линий. 
  
## <a name="syntax"></a>Синтаксис

INTERSECTX (** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *года 2* **, ** *angle2* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Обязательный  <br/> |**Число** <br/> |_X_-координаты точки в первой строке.  <br/> |
| _y1_ <br/> |Обязательный  <br/> |**Число** <br/> |_Y_-координаты точки в первой строке.  <br/> |
| _angle1_ <br/> |Обязательный  <br/> |**Число** <br/> | Значение ячейки угол для первой строки.  <br/> |
| _x2_ <br/> |Обязательный  <br/> |**Число** <br/> |_X_-координаты точки во второй строке.  <br/> |
| _года 2_ <br/> |Обязательный  <br/> |**Число** <br/> |_Y_-координаты точки во второй строке.  <br/> |
| _angle2_ <br/> |Обязательный  <br/> |**Число** <br/> |Значение ячейки угол для второй строке.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Number
  
## <a name="remarks"></a>Замечания

Каждой строки определяется как точка (*x, y*) и угол. 
  
Microsoft Visio использует эту функцию в ячейке PinY связан вращение руководство фигуры. 
  
Если строки не пересекаются, функция возвращает ошибку деление на ноль (#DIV/0!), игнорирует Visio, последний неизвестное значение точки восстановления. 
  
## <a name="example"></a>Пример

INTERSECTY (VertGuide! PinX VertGuide! PinY, VertGuide! Угол HorzGuide! PinX HorzGuide! PinY, HorzGuide! Угол) 
  
Возвращает *y* -координата пересечения точки VertGuide и HorzGuide в единицах страницы. 
  

