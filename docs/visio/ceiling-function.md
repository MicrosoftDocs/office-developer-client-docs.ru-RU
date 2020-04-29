---
title: Функция CEILING
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Округляет число от 0 (нуля) до следующего экземпляра множителя. Если не указано значение Multiple, число округляется от 0 до следующего целого числа.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404129"
---
# <a name="ceiling-function"></a>Функция CEILING

Округляет число от 0 (нуля) до следующего экземпляра _множителя_. Если не указано значение _Multiple_ , число округляется от 0 до следующего целого числа. 
  
## <a name="syntax"></a>Синтаксис

CEILING (* * *число* * * * * * *несколько* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательна  <br/> |**Number** <br/> |Округляемое число.  <br/> |
| _сразу_ <br/> |Обязательна  <br/> |**Number** <br/> |Точность до.  <br/> |
   
## <a name="remarks"></a>Примечания

 _Число_ и _множество_ должны иметь одинаковые знаки или #NUM! возвращается ошибка. Если один или _несколько_ _чисел_ не могут быть преобразованы в значение, то #VALUE! возвращается ошибка. Если один или _несколько_ _чисел_ имеют значение 0, результат равен 0. 
  
## <a name="example-1"></a>Пример 1

CEILING (3.7)
  
Возвращает 4
  
## <a name="example-2"></a>Пример 2

CEILING (-3,7)
  
Возвращает значение — 4
  
## <a name="example-3"></a>Пример 3

CEILING (3.7, 0,25)
  
Возвращает 3,75
  

