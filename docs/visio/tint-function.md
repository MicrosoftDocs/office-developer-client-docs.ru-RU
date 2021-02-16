---
title: Функция TINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Изменяет цвет, увеличив его luminosity на количество (положительное или отрицательное), указанное в параметре int.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406579"
---
# <a name="tint-function"></a>Функция TINT

Изменяет цвет, увеличив его luminosity на количество (положительное или отрицательное), указанное в _параметре int._ 
  
## <a name="syntax"></a>Синтаксис

TINT(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Обязательна  <br/> |**Числовой** <br/> |Индекс цвета Microsoft Visio или RGB-значение цвета.  <br/> |
| _int_ <br/> |Обязательна  <br/> |64-разрядное целое число. <br/> |Количество, на которое увеличивается светоугость цвета. Может быть положительным или отрицательным.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **RGB**
  
## <a name="remarks"></a>Примечания

Верхние и нижние границы luminosity — 0 и 240 соответственно. Для параметра  _int_ не существует ограничений на размер этого параметра, но luminosity никогда не превышает эти ограничения. 
  

