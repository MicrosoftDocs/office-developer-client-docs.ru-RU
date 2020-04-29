---
title: Функция ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Возвращает угол тангенса для пути в заданной точке.
ms.openlocfilehash: 0d38fc0e123a7e38b7826b55415cfc09c1789c0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407328"
---
# <a name="anglealongpath-function"></a>Функция ANGLEALONGPATH

Возвращает угол тангенса для пути в заданной точке.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

ANGLEALONGPATH (* * *раздел* * *, * * *путешествие* * * * * *[, сегмент]* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**String** <br/> |Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).  <br/> |
| _дающих_ <br/> |Обязательна  <br/> |**Double** <br/> |Процентная доля пути от начала до конечной точки. Значение должно находиться в пределах от 0 до 1.  <br/> |
| _segment_ <br/> |Необязательна  <br/> |**Целое число** <br/> |Сегмент на основе 1 пути, по которому вычисляется угол тангенса.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Double**
  
## <a name="remarks"></a>Примечания

Если вы включаете значение _сегмента_ , ANGLEALONGPATH возвращает значение только для этого сегмента. 
  
Если вы включаете значение _сегмента_ , ANGLEALONGPATH определяет точку тангенса с помощью функции _командировок_ для вычисления _сегмента_перцертаже.
  
Если один _раздел_ или _сегмент_ не существует, Microsoft Visio возвращает #REF!. 
  

