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
description: Возвращает целое число от 1-7, представляющее день недели в даты и времени или выражение.
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815166"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY Function (VisioShapeSheet)

Возвращает целое число от 1-7, представляющее день недели в _даты и времени_ или _выражение_.
  
## <a name="syntax"></a>Синтаксис

День НЕДЕЛИ ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _даты и времени_ <br/> |Обязательный  <br/> |**Строка** <br/> | Любая строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.  <br/> |
| _expression_ <br/> |Обязательный  <br/> |**Разные** <br/> |Любое выражение, возвращающее даты и времени.  <br/> |
| _код языка_ <br/> |Optional  <br/> |**Числовой** <br/> |Идентификатор языкового стандарта, который следует использовать для определения нелокальные datetime. Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Целое число
  
## <a name="remarks"></a>Замечания

Компонент времени в _даты и времени_ или _выражение,_ удаляются. 
  
Результат соответствует понедельника воскресенье (7) (1). Округление не выполняется. Если _даты и времени_ , отсутствует или не может использоваться как допустимая дата или время, функция возвращает #VALUE! Ошибка. 
  
Функция WEEKDAY также принимает одно значение номеров для _выражения_ , где целую часть результата представляет число дней, прошедших с 30 декабря 1899. 
  
## <a name="example-1"></a>Пример 1

День НЕДЕЛИ ("30 мая 1999 г.")
  
Возвращает 7.
  
## <a name="example-2"></a>Пример 2

День НЕДЕЛИ (DATEVALUE ("30 мая 1999 г.") + 2 ed.)
  
Возвращает 2.
  
## <a name="example-3"></a>Пример 3

WEEKDAY(35880.6337)
  
Возвращает 4.
  
