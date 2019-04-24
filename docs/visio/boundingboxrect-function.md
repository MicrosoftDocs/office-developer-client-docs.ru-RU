---
title: Функция BOUNDINGBOXRECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Возвращает координату указанного края ограничительной рамки фигуры.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338054"
---
# <a name="boundingboxrect-function"></a>Функция BOUNDINGBOXRECT

Возвращает координату указанного края ограничительной рамки фигуры.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

BOUNDINGBOXRECT (* * *index* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Обязательный  <br/> |**Integer** <br/> |Край ограничительной рамки фигуры, для которой необходимо получить координаты. Возможные значения приведены в разделе reMarks.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Number**
  
## <a name="remarks"></a>Комментарии

 *Индекс* может принимать одно из следующих значений. 
  
|**Item**|**Значение**|
|:-----|:-----|
|Левый край  <br/> |нуль  <br/> |
|Правый край  <br/> |1,1  <br/> |
|Верхняя граница  <br/> |2  <br/> |
|Нижняя граница  <br/> |4  <br/> |
   
Если у фигуры есть родительский объект, возвращаемое значение находится в системе координат родительского элемента.
  

