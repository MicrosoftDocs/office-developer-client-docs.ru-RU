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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341526"
---
# <a name="asin-function"></a>Функция ASIN

Возвращает арксинус числа, например угол, синус которого равен *числу* . 
  
## <a name="syntax"></a>Синтаксис

ASIN (* * *число* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Синус угла.  <br/> |
   
## <a name="remarks"></a>Комментарии

Входное значение должно быть в диапазоне от 1 _Лт_ = *число* _лт_ = 1 или #NUM! возвращается ошибка. Полученный угол находится в диапазоне-Пи/2 _Лт_ = *Angle* _ЛТ_ = PI/2 радиан (-90 _лт_ = *угол* _лт_ = 90 градусов). 
  
## <a name="example"></a>Пример

ASIN (1)
  
Возвращает 90 град
  

