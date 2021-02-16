---
title: Функция FLOOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Округлит число к 0 (ноль), к следующему числу или к следующему экземпляру нескольких.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439900"
---
# <a name="floor-function"></a>Функция FLOOR

Округлит число к 0 (ноль), к следующему числу или к следующему экземпляру  _из_ нескольких.
  
## <a name="syntax"></a>Синтаксис

FLOOR(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательна  <br/> |**Number** <br/> |Число для округли.  <br/> |
| _multiple_ <br/> |Обязательна  <br/> |**Number** <br/> |Кратная, к которой нужно округить.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Числовой
  
## <a name="remarks"></a>Примечания

Если  _не_ указано несколько, число округлится до 0 к следующему числу. 
  
 _Число_ и  _несколько_ должны иметь одинаковые знаки или #NUM! возвращается ошибка. Если  _ни число,_ ни  _несколько_ не могут быть преобразованы в значение, #VALUE! возвращается ошибка. Если число  _или_  _несколько —_ 0, результат будет 0. 
  
## <a name="example-1"></a>Пример 1

FLOOR(3.7)
  
Возвращает 3.
  
## <a name="example-2"></a>Пример 2

FLOOR(-3.7)
  
Возвращает -3.
  
## <a name="example-3"></a>Пример 3

FLOOR(3.7, 0.5)
  
Возвращает 3.5.
  

