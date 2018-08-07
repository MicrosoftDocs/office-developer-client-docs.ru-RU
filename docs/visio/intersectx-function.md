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
description: Возвращает x-координата (в локальной системе координат) точки пересечения двух линий.
ms.openlocfilehash: ea5a08f25f3e45dab3fe3fd83b74cf9a7541b6e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813965"
---
# <a name="intersectx-function"></a>Функция INTERSECTX

Возвращает *x* -координата (в локальной системе координат) точки пересечения двух линий. 
  
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
  
Microsoft Visio использует эту функцию в ячейке PinX связан вращение руководство фигуры. 
  
Если строки не пересекаются, функция возвращает ошибку деление на ноль (#DIV/0!), игнорирует Visio, последний неизвестное значение точки восстановления. 
  
## <a name="example"></a>Пример

INTERSECTX (VertGuide! PinX VertGuide! PinY, VertGuide! Угол HorzGuide! PinX HorzGuide! PinY, HorzGuide! Угол) 
  
Возвращает *x* -координата пересечения точки VertGuide и HorzGuide в единицах страницы. 
  

