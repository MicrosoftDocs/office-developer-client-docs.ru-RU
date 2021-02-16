---
title: Функция BOUNDINGBOXRECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Возвращает координату указанного края границ границ фигуры.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418073"
---
# <a name="boundingboxrect-function"></a>Функция BOUNDINGBOXRECT

Возвращает координату указанного края границ границ фигуры.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

BOUNDINGBOXRECT(** *Index* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Обязательна  <br/> |64-разрядное целое число. <br/> |Край границ границ фигуры, для которого необходимо получить координату. Возможные значения см. в примечаиях.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Number**
  
## <a name="remarks"></a>Примечания

 *Индекс*  может быть одним из следующих значений. 
  
|**Элемент**|**Значение**|
|:-----|:-----|
|Левый край  <br/> |0  <br/> |
|Правый край  <br/> |1   <br/> |
|Верхний край  <br/> |2   <br/> |
|Нижний край  <br/> |3   <br/> |
   
Если фигура имеет родительский, возвращаемая величина находится в системе координат этого родительского.
  

