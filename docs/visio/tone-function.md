---
title: Функция TONE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Изменяет цвет, уменьшая его насыщенность на количество, указанное в параметре int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434377"
---
# <a name="tone-function"></a>Функция TONE

Изменяет цвет, уменьшая его насыщенность на количество, указанное в _параметре int._ 
  
## <a name="syntax"></a>Синтаксис

TONE(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Обязательна  <br/> |**Числовой** <br/> |Индекс цвета Microsoft Visio или RGB-значение цвета.  <br/> |
| _int_ <br/> |Обязательна  <br/> |64-разрядное целое число. <br/> |Количество, с помощью которого уменьшается насыщенность цвета. Может быть положительным или отрицательным.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **RGB**
  
## <a name="remarks"></a>Примечания

Верхние и нижние границы насыщенности — 0 и 240 соответственно. Для параметра int не существует ограничений по размеру, который можно передать для параметра  _int,_ но насыщенность никогда не превышает эти ограничения. 
  

