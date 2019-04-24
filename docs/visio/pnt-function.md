---
title: Функция PNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Возвращает точку, представленную координатами x и y в виде одного значения.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322353"
---
# <a name="pnt-function"></a>Функция PNT

Возвращает точку, представленную координатами _x_ и _y_ в виде одного значения. 
  
## <a name="syntax"></a>Синтаксис

PNT (* * *x, y* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _x, y_ <br/> |Обязательный  <br/> |**Число, число** <br/> |Координаты точки в системе координат текущей фигуры.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Point
  
## <a name="remarks"></a>Замечания

При преобразовании координат в точки можно изменить геометрию фигуры без необходимости управлять координатами *x* и *y* раздельно. 
  
## <a name="example"></a>Пример

PNT (PinX, PinY) 
  
Возвращает точку, представленную PinX и PinY. 
  

