---
title: Функция ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Возвращает угол тангенса для пути в заданной точке.
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160295"
---
# <a name="anglealongpath-function"></a>Функция ANGLEALONGPATH

Возвращает угол тангенса для пути в заданной точке.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

ANGLEALONGPATH (***раздел***, ***путешествие*** ***[, сегмент]*** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**String** <br/> |Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).  <br/> |
| _дающих_ <br/> |Обязательный  <br/> |**Double** <br/> |Процентная доля пути от начала до конечной точки. Значение должно находиться в пределах от 0 до 1.  <br/> |
| _segment_ <br/> |Необязательна  <br/> |**Integer** <br/> |Сегмент на основе 1 пути, по которому вычисляется угол тангенса.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Double**
  
## <a name="remarks"></a>Примечания

Если вы включаете значение _сегмента_ , ANGLEALONGPATH возвращает значение только для этого сегмента. 
  
Если вы включаете значение _сегмента_ , ANGLEALONGPATH определяет точку тангенса с помощью функции _командировок_ для вычисления _сегмента_перцертаже.
  
Если один _раздел_ или _сегмент_ не существует, Microsoft Visio возвращает #REF!. 
  

