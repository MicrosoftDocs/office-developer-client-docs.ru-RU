---
title: Функция ASIN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Возвращает арксинус числа, например угол, синус которого равен числу.
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432823"
---
# <a name="asin-function"></a>Функция ASIN

Возвращает арксинус числа, например угол, синус которого равен *числу* . 
  
## <a name="syntax"></a>Синтаксис

ASIN (* * *число* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательна  <br/> |**Числовой** <br/> |Синус угла.  <br/> |
   
## <a name="remarks"></a>Примечания

Входное значение должно быть в диапазоне от 1 <= *число* <= 1 или #NUM! возвращается ошибка. Полученный угол находится в диапазоне-Пи/2 <= *angle* <= Пи/2 радианы (-90 <= *угол* <= 90 градусов). 
  
## <a name="example"></a>Пример

ASIN (1)
  
Возвращает 90 град
  

