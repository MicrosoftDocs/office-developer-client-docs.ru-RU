---
title: Функция ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Возвращает угол касающегося на путь в данной точке.
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160295"
---
# <a name="anglealongpath-function"></a>Функция ANGLEALONGPATH

Возвращает угол касающегося на путь в данной точке.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

ANGLEALONGPATH ***(раздел***, ***путешествия*** ***[,сегмент]*** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**String** <br/> |Раздел Геометрия, который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).  <br/> |
| _путешествия_ <br/> |Обязательный  <br/> |**Double** <br/> |Процент по пути от точки начала до конца. Должно быть от 0 до 1.  <br/> |
| _segment_ <br/> |Необязательный  <br/> |**Integer** <br/> |1-й сегмент пути для вычисления касающегося угла.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Double**
  
## <a name="remarks"></a>Примечания

Если вы включаете  _значение сегмента,_ ANGLEALONGPATH возвращает значение только для этого сегмента. 
  
Если вы включаете значение _сегмента,_ ANGLEALONGPATH определяет точку касательной с помощью перемещения для вычисления перцертажа вдоль _сегмента_. 
  
Если раздел _или_ _сегмент_ не существует, корпорация Майкрософт Visio возвращает #REF!. 
  

