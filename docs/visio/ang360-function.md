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
ms.openlocfilehash: 6916e50daad735843bf0a2a6361fb5b1b833e2ce
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160302"
---
# <a name="ang360-function"></a>Функция ANG360

Нормализует диапазон угла в 0 \< = результат \< 2PI радиансов (0 \< = результат \< 360 градусов).
  
## <a name="syntax"></a>Синтаксис

ANG360 ***(угол*** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _угол_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Угол, который необходимо нормализовать.  <br/> |
   
## <a name="remarks"></a>Примечания

Если  *угол*  не указывается с помощью угловых единиц, он интерпретируется как радианы. Если  *угол*  не может быть преобразован в значение, #VALUE! возвращается ошибка. 
  
## <a name="example-1"></a>Пример 1

ANG360 (395 дег)
  
Возвращает 35 дег
  
## <a name="example-2"></a>Пример 2

ANG360 (-9.8 rad)
  
Возвращает 2.7664 rad
  
## <a name="example-3"></a>Пример 3

ANG360 (45)
  
Возвращает 58.31 дег (1.0177 rad)
  

