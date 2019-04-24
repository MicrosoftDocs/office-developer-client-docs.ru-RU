---
title: Функция MSOTINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Изменяет цвет, увеличивая его яркость на указанный процент.
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335198"
---
# <a name="msotint-function"></a>Функция MSOTINT

Изменяет цвет, увеличивая его яркость на указанный процент.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

MSOTINT (* * *Color* * *, * * *делталум* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Обязательный  <br/> |**RGB** <br/> |Стандартное значение цвета RGB (красный, зеленый, синий) или ссылка на цвет.  <br/> |
| _Делталум_ <br/> |Обязательный  <br/> |**Integer** <br/> |Процент изменения в сторону белого (-100%) или Black (100%) из значения _цвета_ .  <br/> |
   
## <a name="remarks"></a>Комментарии

Чем ближе значение _цвета_ к белому или черному, тем меньше изменяется оттенок, который создается определенным значением _делталум_ . 
  

