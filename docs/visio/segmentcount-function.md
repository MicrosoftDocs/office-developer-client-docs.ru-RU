---
title: Функция SEGMENTCOUNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Возвращает число отрезков, составляющих путь.
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814753"
---
# <a name="segmentcount-function"></a>Функция SEGMENTCOUNT

Возвращает число отрезков, составляющих путь.
  
## <a name="syntax"></a>Синтаксис

SEGMENTCOUNT (** *pathRef* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |Обязательный  <br/> |**Integer** <br/> |Раздел геометрии, представляющий путь, указанный с помощью ссылки на ячейки путь (например, Geometry1.Path).  <br/> |
   
### <a name="return-value"></a>������������ ��������

Целое число
  
## <a name="remarks"></a>Замечания

Пересечения линий не включаются в общее число возвращаемых сегменты.
  

