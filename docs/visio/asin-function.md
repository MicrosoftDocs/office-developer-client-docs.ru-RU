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
description: Возвращает arcsine числа, например, угол, чей sine является номером .
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293508"
---
# <a name="asin-function"></a>Функция ASIN

Возвращает arcsine числа, например, угол, чей sine является  *номером*  . 
  
## <a name="syntax"></a>Синтаксис

ASIN ***(номер)*** 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Sine угла.  <br/> |
   
## <a name="remarks"></a>Примечания

Значение ввода должно быть в диапазоне -1 <=  *номер*  <= 1 или #NUM! возвращается ошибка. В результате угол находится в диапазоне -PI/2 < *=*  угол <= радианы PI/2 (-90 < *=*  угол <= 90 градусов). 
  
## <a name="example"></a>Пример

ASIN (1)
  
Возвращает 90 дег
  

