---
title: Функция ANG360
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Нормализует диапазон угла.
ms.openlocfilehash: 01092e06b55c73953417fe7d0fa1c9f74d668922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813144"
---
# <a name="ang360-function"></a>Функция ANG360

Нормализует диапазон угла до 0 \<= результатов \< 2PI радианах (0 \<= результатов \< 360 градусов).
  
## <a name="syntax"></a>Синтаксис

ANG360 (** *угол* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _угол_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Угол, чтобы он был нормализован.  <br/> |
   
## <a name="remarks"></a>Замечания

Если *угол* не указан с помощью угловые единиц измерения, он интерпретируется в радианах. Если значение #VALUE не может быть преобразована *угол* ! возвращается ошибка. 
  
## <a name="example-1"></a>Пример 1

ANG360(395 deg)
  
Возвращает 35 градусов
  
## <a name="example-2"></a>Пример 2

ANG360(-9.8 RAD)
  
Возвращает 2.7664 rad
  
## <a name="example-3"></a>Пример 3

ANG360(45)
  
Возвращает 58.31 градусов (1.0177 rad)
  

