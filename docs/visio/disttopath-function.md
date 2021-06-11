---
title: Функция DISTTOPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Возвращает самое короткое расстояние от точки, представленной указанными координатами, в точку на пути.
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427019"
---
# <a name="disttopath-function"></a>Функция DISTTOPATH

Возвращает самое короткое расстояние от точки, представленной указанными координатами, в точку на пути.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

DISTTOPATH(** *раздел* **, ** *x* **, ** *y* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**String** <br/> |Раздел Геометрия, который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).  <br/> |
| _x_ <br/> |Обязательный  <br/> |**Double** <br/> |X-координата точки.   <br/> |
| _y_ <br/> |Обязательный  <br/> |**Double** <br/> |_Y-координата_ точки.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Double**
  
## <a name="remarks"></a>Примечания

Microsoft Visio возвращает #REF! если  _раздел_ не существует. 
  
Возвращаемая величина является положительной, если точка находится слева от направления перемещения; это отрицательно, если точка находится справа от направления перемещения.
  

