---
title: Функция NEARESTPOINTONPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Возвращает процентное отношение расстояния вдоль пути к точке, ближайшей к заданным координатам, в виде значения от 0 до 1.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319721"
---
# <a name="nearestpointonpath-function"></a>Функция NEARESTPOINTONPATH

Возвращает процентное отношение расстояния вдоль пути к точке, ближайшей к заданным координатам, в виде значения от 0 до 1.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

NEARESTPOINTONPATH (* * *раздел* * *, * * *x* * *, * * *y* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**String** <br/> |Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).  <br/> |
| _x_ <br/> |Обязательный  <br/> |**Double** <br/> |Координата _x_указанной точки.  <br/> |
| _y_ <br/> |Обязательный  <br/> |**Double** <br/> |Координата _y_указанной точки.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Double**
  
## <a name="remarks"></a>Замечания

Если _раздел_ не существует, Microsoft Visio возвращает #REF!. 
  

