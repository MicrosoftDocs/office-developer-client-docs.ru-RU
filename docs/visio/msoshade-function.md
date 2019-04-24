---
title: Функция MSOSHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Изменяет цвет, уменьшая яркость на указанный процент.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283712"
---
# <a name="msoshade-function"></a>Функция MSOSHADE

Изменяет цвет, уменьшая яркость на указанный процент.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

MSOSHADE (* * *Color* * *, * * *-делталум* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Обязательный  <br/> |**RGB** <br/> |Стандартное значение цвета RGB (красный, зеленый, синий) или ссылка на цвет.  <br/> |
| _— Делталум_ <br/> |Обязательный  <br/> |**Integer** <br/> |Процент изменения в сторону белого (-100%) или Black (100%) из значения _цвета_ .  <br/> |
   
## <a name="remarks"></a>Замечания

Чем ближе значение _цвета_ к белому или черному, тем меньше изменяется затенение, созданное определенным значением _делталум_ . 
  

