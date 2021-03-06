---
title: Функция NEARESTPOINTONPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Возвращает процент расстояния по пути точки, ближайшей к указанным координатам, в качестве значения от 0 до 1.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407335"
---
# <a name="nearestpointonpath-function"></a>Функция NEARESTPOINTONPATH

Возвращает процент расстояния по пути точки, ближайшей к указанным координатам, в качестве значения от 0 до 1.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

NEARESTPOINTONPATH(** *раздел* **, ** *x* **, ** *y* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**String** <br/> |Раздел Геометрия, который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).  <br/> |
| _x_ <br/> |Обязательный  <br/> |**Double** <br/> |X-координата указанной точки.   <br/> |
| _y_ <br/> |Обязательный  <br/> |**Double** <br/> |Y-координата указанной точки.   <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Double**
  
## <a name="remarks"></a>Примечания

Если _раздел_ не существует, корпорация Майкрософт Visio возвращает #REF!. 
  

