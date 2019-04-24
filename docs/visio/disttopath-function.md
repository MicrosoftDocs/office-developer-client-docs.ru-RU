---
title: Функция DISTTOPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Возвращает наименьшее расстояние от точки, представленной указанными координатами, к точке пути.
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332692"
---
# <a name="disttopath-function"></a>Функция DISTTOPATH

Возвращает наименьшее расстояние от точки, представленной указанными координатами, к точке пути.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

DISTTOPATH (* * *раздел* * *, * * *x* * *, * * *y* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**String** <br/> |Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).  <br/> |
| _x_ <br/> |Обязательный  <br/> |**Double** <br/> |Координата _x_точки.  <br/> |
| _y_ <br/> |Обязательный  <br/> |**Double** <br/> |Координата _y_точки.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Double**
  
## <a name="remarks"></a>Комментарии

Microsoft Visio возвращает #REF! Если _раздел_ не существует. 
  
Возвращаемое значение является положительным, если точка находится слева от направления поездки; оно отрицательно, если точка находится справа от направления поездки.
  

