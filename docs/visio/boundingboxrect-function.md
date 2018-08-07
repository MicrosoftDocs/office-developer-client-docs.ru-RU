---
title: Функция BOUNDINGBOXRECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Возвращает координаты указанного краю фигуры, ограничивающего поля.
ms.openlocfilehash: 2c850cb213ec0093ead53cd860f92e38da46f27e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813305"
---
# <a name="boundingboxrect-function"></a>Функция BOUNDINGBOXRECT

Возвращает координаты указанного краю фигуры, ограничивающего поля.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

BOUNDINGBOXRECT (** *индекса* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Обязательный  <br/> |**Integer** <br/> |Край фигуры прямоугольника для которого необходимо получить координаты. Возможные значения см.  <br/> |
   
### <a name="return-value"></a>������������ ��������

 **Число**
  
## <a name="remarks"></a>Замечания

 *Индекс* может иметь одно из следующих значений. 
  
|**Элемент**|**Значение**|
|:-----|:-----|
|Левые края  <br/> |0  <br/> |
|Правые края  <br/> |1  <br/> |
|Верхняя граница  <br/> |2  <br/> |
|Нижний край  <br/> |3  <br/> |
   
Если фигура имеет родительский объект, возвращается в системе координат родительской.
  

