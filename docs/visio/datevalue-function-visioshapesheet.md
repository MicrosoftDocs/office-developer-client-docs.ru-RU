---
title: DATEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Возвращает значение даты, представленное датой или выражением.
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360314"
---
# <a name="datevalue-function-visioshapesheet"></a>DATEVALUE Function (VisioShapeSheet)

Возвращает значение даты, представленное датой _или_ _выражением._
  
## <a name="syntax"></a>Синтаксис

DATEVALUE(" ** *datetime* ** "| ** *выражение* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Обязательный  <br/> |**String** <br/> |Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.  <br/> |
| _expression_ <br/> |Обязательный  <br/> |**String** <br/> |Любое выражение, возвращающее дату и время.  <br/> |
| _lcid_ <br/> |Необязательный  <br/> |**Number** <br/> |Указывает идентификатор локального адреса, который будет использоваться для оценки неместного времени даты. Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Datetime
  
## <a name="remarks"></a>Примечания

Любой компонент времени в  *дате*  или  *выражении*  отбрасывается. 
  
Если  *дата отсутствует*  или не может быть преобразована в допустимый результат, DATEVALUE возвращает #VALUE! ошибка. 
  
Возвращенное значение отображается с помощью стиля короткой даты, установленного текущим региональным Параметры. 
  
Функция DATEVALUE также принимает одно значение  номера для выражения, в котором вся часть результата представляет дни с 30 декабря 1899 г. 
  
## <a name="example-1"></a>Пример 1

DATEVALUE (NOW( ))+5 ed.
  
Возвращает дату через пять дней.
  
## <a name="example-2"></a>Пример 2

DATEVALUE ("7/19/1995 12:30")
  
Возвращает дату.
  
## <a name="example-3"></a>Пример 3

DATEVALUE ("33 мая 1997 г.")
  
Возвращает #VALUE! ошибка.
  
## <a name="example-4"></a>Пример 4

DATEVALUE (35580.6337)
  
Возвращает 5/30/1997.
  

