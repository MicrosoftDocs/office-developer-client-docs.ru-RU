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
description: Возвращает точку, представленную координатами x и y в качестве единого значения.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435714"
---
# <a name="pnt-function"></a>Функция PNT

Возвращает точку, представленную координатами  _x_ и  _y_ в качестве единого значения. 
  
## <a name="syntax"></a>Синтаксис

PNT(** *x,y* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _x,y_ <br/> |Обязательный  <br/> |**Номер, номер** <br/> |Координаты точки в системе координат текущей формы.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Point
  
## <a name="remarks"></a>Примечания

Преобразование координат в точки позволяет изменять геометрию фигуры без необходимости манипулировать  *х*  и  *y-координатами*  отдельно. 
  
## <a name="example"></a>Пример

PNT(PinX,Piny) 
  
Возвращает точку, представленную PinX и PinY. 
  

