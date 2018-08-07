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
description: Округляет число до точности, представленное усеченное.
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19814637"
---
# <a name="round-function-visioshapesheet"></a>ROUND Function (VisioShapeSheet)

Округляет число до точности, представленное *усеченное* . 
  
## <a name="syntax"></a>Синтаксис

ROUND (** *номер* **, ** *усеченное* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Обязательный  <br/> |**Число** <br/> |Номер для округления.  <br/> |
| _усеченное_ <br/> |Обязательный  <br/> |**Число** <br/> |Число десятичных разрядов точности.  <br/> |
   
## <a name="remarks"></a>Замечания

Если _усеченное_ больше 0, _число_ округляется с _усеченное_ справа от десятичной запятой. Если _усеченное_ равно 0, _число_ округляется до целого числа. Если _усеченное_ меньше 0, _число_ округляется с _усеченное_ слева от десятичной запятой. 
  
## <a name="example-1"></a>Пример 1

ROUND(123.654,2)
  
Возвращает 123.65.
  
## <a name="example-2"></a>Пример 2

ROUND(123.654,0)
  
Возвращает 124.
  
## <a name="example-3"></a>Пример 3

ROUND(123.654,-1)
  
Возвращает 120.
  

