---
title: Функция MSOSHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Изменяет цвет, уменьшая его светоносность на указанный процент.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414496"
---
# <a name="msoshade-function"></a>Функция MSOSHADE

Изменяет цвет, уменьшая его светоносность на указанный процент.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

MSOSHADE(** *цвет* **, ** *-deltaLum* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Обязательный  <br/> |**RGB** <br/> |Стандартное значение RGB (красный, зеленый, синий) или ссылка на цвет.  <br/> |
| _-deltaLum_ <br/> |Обязательный  <br/> |**Integer** <br/> |Процентное изменение в сторону белого (-100%) или черный (100%) из _значения цвета._  <br/> |
   
## <a name="remarks"></a>Примечания

Чем _ближе_ значение цвета к белому или черному, тем меньше изменение в тени, которое производится определенным _значением deltaLum._ 
  

