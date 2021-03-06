---
title: Функция ATAN2
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Возвращает угол между вектором, представленным x,y, и направлением x-axis. Результатом является число в текущем единице измерения для углов.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436484"
---
# <a name="atan2-function"></a>Функция ATAN2

Возвращает угол между вектором, представленным *x,y,* и направлением *x-axis.* Результатом является число в текущем единице измерения для углов. 
  
## <a name="syntax"></a>Синтаксис

ATAN2(** *y* **, ** *x* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Значение  _y-value_ точки.  <br/> |
| _x_ <br/> |Обязательный  <br/> |**Числовой** <br/> |_X-значение_ точки.  <br/> |
   
## <a name="remarks"></a>Примечания

Arctangent — это угол, измеренный против часовой стрелки от положительной оси  *x-axis*  до линии, пересекающей происхождение (0,0) и точку, представленную  *x*  и  *y*  . В microsoft Visio ATAN2 (0,0) возвращает 0. Чтобы заставить результат ATAN2 в другое угловое измерение, используйте функцию DEG или RAD. 
  
Функция ATAN2 — это антифункция функции TAN. Функция ATAN2 возвращает угол, угол которого равен *y,* разделенным *на x.* Если ATAN2 *(y,x)* представляет угол в правом треугольнике,  *y*  является "противоположной стороной", а  *x*  — "смежной стороной", поэтому функция может быть написана как ATAN2 (напротив, смежная). 
  
## <a name="example-1"></a>Пример 1

ATAN2 (1.25,2.25)
  
Возвращает 29.0456 дег
  
## <a name="example-2"></a>Пример 2

ATAN2(1, SQRT(3))
  
Возвращает 30 дег
  
## <a name="example-3"></a>Пример 3

ATAN2 (1,1)
  
Возвращает 45 дег
  

