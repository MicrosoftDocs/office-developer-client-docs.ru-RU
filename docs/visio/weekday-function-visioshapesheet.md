---
title: WEEKDAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Возвращает integer, от 1 до 7, представляющее день недели в дате или выражении.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404808"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY Function (VisioShapeSheet)

Возвращает integer, от 1 до 7, представляющее день недели в  _даты и времени_ или  _выражение_.
  
## <a name="syntax"></a>Синтаксис

WEEKDAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Обязательно  <br/> |**Строка** <br/> | Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.  <br/> |
| _expression_ <br/> |Обязательный  <br/> |**Разные** <br/> |Любое выражение, возвращающее дату и время.  <br/> |
| _lcid_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Идентификатор языкового стандарта, используемый при оценке нелокальных даты и времени. Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Целое число
  
## <a name="remarks"></a>Замечания

Из параметров _datetime_ и _expression_ удаляется компонент времени. 
  
Результат соответствует понедельнику (1) по воскресенье (7). Округление не выполняется. Если  _дата-время_ отсутствует или не может быть интерпретирована как допустимая дата или время, функция возвращает #VALUE! error. 
  
Функция WEEKDAY также принимает одно число  для выражения, где значительная часть результата представляет количество дней с 30 декабря 1899 г. 
  
## <a name="example-1"></a>Пример 1

WEEKDAY ("30 мая 1999 г.")
  
Возвращает 7.
  
## <a name="example-2"></a>Пример 2

WEEKDAY(DATEVALUE("30 мая 1999 г.")+2 ed.)
  
Возвращает 2.
  
## <a name="example-3"></a>Пример 3

WEEKDAY(35880.6337)
  
Возвращает 4.
  

