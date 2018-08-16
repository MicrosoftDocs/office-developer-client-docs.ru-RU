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
description: Возвращает целое число от 0 до 23, представляющее час дня даты и времени или выражения.
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813916"
---
# <a name="hour-function-visioshapesheet"></a>HOUR Function (VisioShapeSheet)

Возвращает целое число от 0 до 23, представляющее час дня _даты и времени_ или _выражения_.
  
## <a name="syntax"></a>Синтаксис

ЧАС ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _даты и времени_ <br/> |Обязательный  <br/> |**Строка** <br/> | Строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.  <br/> |
| _expression_ <br/> |Обязательный  <br/> |**Разные** <br/> |Выражение, возвращающее даты и времени.  <br/> |
| _код языка_ <br/> |Optional  <br/> |**Число** <br/> | Идентификатор языкового стандарта, который следует использовать для определения нелокальные datetime. Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.  <br/> |
   
## <a name="remarks"></a>Замечания

Удаляется компонент даты в *даты и времени* и *выражение* . 
  
Округление не выполняется. Если *даты и времени* , отсутствует или не может быть преобразована допустимый результат, функция возвращает ошибку. 
  
Возвращаемое значение форматируется в соответствии с формат времени, задание с текущих региональных параметров компьютера. 
  
Функция HOUR также принимает одно значение номеров для *выражения* , где целой и дробной части результат представляет долю день после полночи. 
  
## <a name="example-1"></a>Пример 1

HOUR("15:45")
  
Возвращает 15.
  
## <a name="example-2"></a>Пример 2

ЧАС ("30 мая 1997 г., 15:45:24 часов")
  
Возвращает 15.
  
## <a name="example-3"></a>Пример 3

HOUR(0.5)
  
Возвращает 12.
  
## <a name="example-4"></a>Пример 4

HOUR("5/30/1997")
  
Возвращает 0.
  
