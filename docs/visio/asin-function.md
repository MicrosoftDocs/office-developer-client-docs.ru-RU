---
title: Функция ASIN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Возвращает арксинус числа, например, угол, синус которого равен числу.
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813185"
---
# <a name="asin-function"></a>Функция ASIN

Возвращает арксинус числа, например, угол, синус которого равен *числу* . 
  
## <a name="syntax"></a>Синтаксис

ASIN (** *номер* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Синус угла.  <br/> |
   
## <a name="remarks"></a>Замечания

Входное значение должно быть в диапазоне от -1 < = *номер* < = 1 или #NUM! возвращается ошибка. Полученного угла находится в диапазоне -ПИ/2 < = *угол* < = пи/2 радианов (-90 < = *угол* < = 90 градусов). 
  
## <a name="example"></a>Пример

ASIN(1)
  
Возвращает 90 градусов
  

