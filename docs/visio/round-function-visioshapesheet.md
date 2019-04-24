---
title: ROUND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Округляет число до точности, представленной нумберофдигитс.
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315577"
---
# <a name="round-function-visioshapesheet"></a>ROUND Function (VisioShapeSheet)

Округляет число до точности, представленной *нумберофдигитс* . 
  
## <a name="syntax"></a>Синтаксис

ROUND (* * *число* * *, * * *нумберофдигитс* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательный  <br/> |**Number** <br/> |Число, которое требуется округлить.  <br/> |
| _нумберофдигитс_ <br/> |Обязательный  <br/> |**Number** <br/> |Число десятичных разрядов точности.  <br/> |
   
## <a name="remarks"></a>Замечания

Если _нумберофдигитс_ больше 0, _число_ округляется на _нумберофдигитс_ справа от десятичного разделителя. Если значение _нумберофдигитс_ равно 0, то _число_ округляется до целого числа. Если _нумберофдигитс_ меньше 0, _число_ округляется с _нумберофдигитс_ слева от десятичного разделителя. 
  
## <a name="example-1"></a>Пример 1

ROUND (123.654, 2)
  
Возвращает 123,65.
  
## <a name="example-2"></a>Пример 2

ROUND (123.654, 0)
  
Возвращает 124.
  
## <a name="example-3"></a>Пример 3

ROUND (123.654,-1)
  
Возвращает 120.
  

