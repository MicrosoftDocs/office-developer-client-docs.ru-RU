---
title: Функция PATHLENGTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Возвращает длину пути, определенного в указанном разделе "Геометрия".
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405851"
---
# <a name="pathlength-function"></a>Функция PATHLENGTH

Возвращает длину пути, определенного в указанном разделе "Геометрия".
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

PATHLENGTH(** *section* ** ** *[,segment]* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательно  <br/> |**Строка** <br/> |Раздел "Геометрия", который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).  <br/> |
| _segment_ <br/> |Необязательна  <br/> |64-разрядное целое число. <br/> |Сегмент пути для измерения на основе 1.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 64-разрядное число с плавающей запятой двойной точности.
  
## <a name="remarks"></a>Примечания

Если  _раздел_ или  _сегмент_ не существует, Microsoft Visio возвращает #REF!. 
  
Если у вас есть  _значение сегмента,_ PATHLENGTH возвращает только длину этого сегмента. 
  

