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
ms.openlocfilehash: 017dd89bd3b814c10422cd32eea1ee7e343eaf50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341491"
---
# <a name="ang360-function"></a>Функция ANG360

Нормализует диапазон \<угла до 0 = результат \< 2pi радиан (0 \<= результат \< 360 градусов).
  
## <a name="syntax"></a>Синтаксис

ANG360 (* * *угол* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _градусов_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Угол для нормализации.  <br/> |
   
## <a name="remarks"></a>Комментарии

Если *угол* не указан с помощью угловых единиц, он интерпретируется как радианы. Если *угол* не может быть преобразован в значение, то #VALUE! возвращается ошибка. 
  
## <a name="example-1"></a>Пример 1

ANG360 (395 градусов)
  
Возвращает 35 град
  
## <a name="example-2"></a>Пример 2

ANG360 (-9,8 RAD)
  
Возвращает 2,7664 RAD
  
## <a name="example-3"></a>Пример 3

ANG360 (45)
  
Возвращает 58,31 град (1,0177 RAD)
  

