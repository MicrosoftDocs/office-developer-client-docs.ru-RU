---
title: SECOND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Возвращает количество от 0 до 59, которое представляет собой компонент секунд даты и времени или выражения.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404878"
---
# <a name="second-function-visioshapesheet"></a>SECOND Function (VisioShapeSheet)

Возвращает количество от 0 до 59, которое представляет компонент секунд _даты и времени_ или _выражения._
  
## <a name="syntax"></a>Синтаксис

SECOND(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Обязательно  <br/> |**Строка** <br/> |Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.  <br/> |
| _expression_ <br/> |Обязательно  <br/> |**Строка** <br/> | Любое выражение, возвращающее дату и время.  <br/> |
| _lcid_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Идентификатор локали, используемый при оценке нелокального _времени даты и времени._ Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Целое число
  
## <a name="remarks"></a>Замечания

Компонент даты в  _дате или_  _выражении_ удаляется. 
  
Округление не выполняется. Если  _дата-время_ отсутствует или не удается преобразовать в допустимый результат, эта функция возвращает ошибку. 
  
Second function also accepts a single number value for  _expression_ where the decimal part of the result represents the fraction of a day since midnight. 
  
## <a name="example-1"></a>Пример 1

SECOND("05/30/1997 13:45:32")
  
Возвращает 32.
  
## <a name="example-2"></a>Пример 2

SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)
  
Возвращает 52.
  
## <a name="example-3"></a>Пример 3

SECOND(0.6337)
  
Возвращает 32.
  

