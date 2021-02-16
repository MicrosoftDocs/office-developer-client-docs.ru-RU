---
title: Функция ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Возвращает угол тангента в путь в заданной точке.
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160295"
---
# <a name="anglealongpath-function"></a>Функция ANGLEALONGPATH

Возвращает угол тангента в путь в заданной точке.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

ANGLEALONGPATH(***section***, ***travel*** ***[,segment]*** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательно  <br/> |**Строка** <br/> |Раздел "Геометрия", который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).  <br/> |
| _travel_ <br/> |Обязательна  <br/> |64-разрядное число с плавающей запятой двойной точности. <br/> |Процент вдоль пути от точки начала до конца. Должно быть от 0 до 1.  <br/> |
| _segment_ <br/> |Необязательна  <br/> |64-разрядное целое число. <br/> |Сегмент пути на основе 1, по которому вычисляется угол тангента.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 64-разрядное число с плавающей запятой двойной точности.
  
## <a name="remarks"></a>Примечания

Если у вас есть  _значение сегмента,_ ANGLEALONGPATH возвращает значение только для этого сегмента. 
  
Если вы _включаете_ значение сегмента, ANGLEALONGPATH определяет точку тангенса с помощью перемещения для вычисления перцеrtage вдоль _сегмента._ 
  
Если раздел  _или_  _сегмент_ не существует, Microsoft Visio возвращает #REF!. 
  

