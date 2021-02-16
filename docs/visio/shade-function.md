---
title: Функция SHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Изменяет цвет, уменьшая его свет на количество (положительное или отрицательное), указанное в параметре int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326601"
---
# <a name="shade-function"></a>Функция SHADE

Изменяет цвет, уменьшая его свет на количество (положительное или отрицательное), указанное в _параметре int._ 
  
## <a name="syntax"></a>Синтаксис

SHADE(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Обязательна  <br/> |**Числовой** <br/> |Индекс цвета Microsoft Visio или RGB-значение цвета.  <br/> |
| _int_ <br/> |Обязательна  <br/> |64-разрядное целое число. <br/> |Количество, с помощью которого уменьшается светоугость цвета. Может быть положительным или отрицательным.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **RGB**
  
## <a name="remarks"></a>Примечания

Верхние и нижние границы luminosity — 0 и 240 соответственно. Для параметра int не существует ограничений на размер допустимого  _integer,_ но luminosity никогда не превышает эти ограничения. 
  
![Верхние и нижние границы luminosity](media/image199_ZA10173627.gif)
  

