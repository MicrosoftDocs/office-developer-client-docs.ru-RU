---
title: Функция SHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Изменяет цвет, уменьшая яркость на величину (положительное или отрицательное), указанный в параметре int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382983"
---
# <a name="shade-function"></a>Функция SHADE

Изменяет цвет, уменьшая яркость на величину (положительное или отрицательное), указанный в параметре _int_ . 
  
## <a name="syntax"></a>Синтаксис

ЗАЛИВКА (** *цвет* **, ** *int* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Цвет_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Microsoft Visio цветовой индекс или значение цвета RGB.  <br/> |
| _int_ <br/> |Обязательный  <br/> |**Integer** <br/> |Значение, на которое уменьшение яркости цвета. Может быть положительным или отрицательным.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **RGB**
  
## <a name="remarks"></a>Замечания

Верхние и нижние границ «яркость» — 0 и 240 соответственно. Ограничения на размер целое число, которое можно передать для параметра _int_ , не существует, но яркость никогда не превышает эти ограничения. 
  
![Верхний и нижний пределы яркости](media/image199_ZA10173627.gif)
  

