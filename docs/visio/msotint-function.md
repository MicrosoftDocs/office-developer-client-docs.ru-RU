---
title: Функция MSOTINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Изменяет цвет, увеличивает яркость, в процентах.
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814317"
---
# <a name="msotint-function"></a>Функция MSOTINT

Изменяет цвет, увеличивает яркость, в процентах.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010 
  
## <a name="syntax"></a>Синтаксис

MSOTINT (** *цвет* **, ** *deltaLum* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Цвет_ <br/> |Обязательный  <br/> |**RGB** <br/> |Стандартная значение цвета RGB (красный, зеленый, синий) или ссылку на цвет.  <br/> |
| _deltaLum_ <br/> |Обязательный  <br/> |**Integer** <br/> |Изменения в процентах к Технический (-100%) или черным (100%) из значение _цвета_ .  <br/> |
   
## <a name="remarks"></a>Замечания

Более подробно, значение _цвета_ Технический или черного, тем меньше изменения tint, формируемого с определенным _deltaLum_ значение. 
  

