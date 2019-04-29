---
title: Функция SEGMENTCOUNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Возвращает количество сегментов линии, составляющих путь.
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424499"
---
# <a name="segmentcount-function"></a>Функция SEGMENTCOUNT

Возвращает количество сегментов линии, составляющих путь.
  
## <a name="syntax"></a>Синтаксис

SEGMENTCOUNT (* * *пасреф* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Пасреф_ <br/> |Обязательный  <br/> |**Integer** <br/> |Раздел геометрии, представляющий путь, заданный с помощью ячейки ссылки на путь (например, Geometry1. Path).  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Целое число
  
## <a name="remarks"></a>Замечания

Пересечения линий не включаются в общее число возвращенных сегментов.
  

