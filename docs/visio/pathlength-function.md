---
title: Функция PATHLENGTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Возвращает длину пути, определенного в указанном разделе геометрии.
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344417"
---
# <a name="pathlength-function"></a>Функция PATHLENGTH

Возвращает длину пути, определенного в указанном разделе геометрии.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

PATHLENGTH (* * *раздел* * * * * *[, сегмент]* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**String** <br/> |Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).  <br/> |
| _сегмент_ <br/> |Необязательно заполнять.  <br/> |**Integer** <br/> |Сегмент на основе единицы измерения пути для измерения.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Double**
  
## <a name="remarks"></a>Комментарии

Если _раздел_ или _сегмент_ не существует, Microsoft Visio возвращает #REF!. 
  
Если вы включаете значение _сегмента_ , PATHLENGTH возвращает длину только этого сегмента. 
  

