---
title: HOUR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Возвращается в несколько часов от 0 до 23, представляющее час дня даты или выражения.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429637"
---
# <a name="hour-function-visioshapesheet"></a>HOUR Function (VisioShapeSheet)

Возвращает в нее несколько часов от 0 до 23, представляющее час дня даты _или_ _выражения._
  
## <a name="syntax"></a>Синтаксис

HOUR(" ** *datetime* ** "| ** *выражение* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Обязательный  <br/> |**String** <br/> | Строка, обычно распознаемая как дата и время или ссылка на ячейку, содержащую дату и время.  <br/> |
| _expression_ <br/> |Обязательный  <br/> |**Разные** <br/> |Выражение, которое дает дату и время.  <br/> |
| _lcid_ <br/> |Необязательный  <br/> |**Number** <br/> | Идентификатор locale, который будет использоваться для оценки нелокального времени даты. Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.  <br/> |
   
## <a name="remarks"></a>Примечания

Компонент даты в  *дате*  и  *выражении*  удаляется. 
  
Округление не выполняется. Если время  *даты*  отсутствует или не может быть преобразовано в допустимый результат, функция возвращает ошибку. 
  
Возвращенное значение отформатировано в соответствии со стилем времени, установленным текущим региональным Параметры. 
  
Функция HOUR также принимает одно значение  номера для выражения, где десятичная часть результата представляет долю дня с полуночи. 
  
## <a name="example-1"></a>Пример 1

HOUR ("15:45")
  
Возвращает 15.
  
## <a name="example-2"></a>Пример 2

HOUR ("30 мая 1997 г. 15:45:24")
  
Возвращает 15.
  
## <a name="example-3"></a>Пример 3

HOUR (0.5)
  
Возвращает 12.
  
## <a name="example-4"></a>Пример 4

HOUR ("5/30/1997")
  
Возвращает 0.
  

