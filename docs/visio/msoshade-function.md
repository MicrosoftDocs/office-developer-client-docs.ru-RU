---
title: Функция MSOSHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Изменяет цвет, уменьшая яркость указанную часть.
ms.openlocfilehash: f5f6eb0b6009473dcec017e951cca2f90b6c4d55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814288"
---
# <a name="msoshade-function"></a>Функция MSOSHADE

Изменяет цвет, уменьшая яркость указанную часть.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

MSOSHADE (** *цвет* **, ** *- deltaLum* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Цвет_ <br/> |Обязательный  <br/> |**RGB** <br/> |Стандартная значение цвета RGB (красный, зеленый, синий) или ссылку на цвет.  <br/> |
| _-deltaLum_ <br/> |Обязательный  <br/> |**Integer** <br/> |Изменения в процентах к Технический (-100%) или черным (100%) из значение _цвета_ .  <br/> |
   
## <a name="remarks"></a>Замечания

Более подробно, значение _цвета_ Технический или черного, тем меньше изменения тень, формируемого с определенным _-deltaLum_ значение. 
  

