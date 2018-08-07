---
title: Функция DISTTOPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Возвращает короткий расстояние от точки, представленной по указанным координатам точку на пути.
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813632"
---
# <a name="disttopath-function"></a>Функция DISTTOPATH

Возвращает короткий расстояние от точки, представленной по указанным координатам точку на пути.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

DISTTOPATH (** *раздел* **, ** *x* **, ** *y* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**Строка** <br/> |Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).  <br/> |
| _x_ <br/> |Обязательный  <br/> |**Double** <br/> |_X_-координаты точки.  <br/> |
| _y_ <br/> |Обязательный  <br/> |**Double** <br/> |_Y_-координаты точки.  <br/> |
   
### <a name="return-value"></a>������������ ��������

 **Double**
  
## <a name="remarks"></a>Замечания

Microsoft Visio возвращает #REF! Если _раздел_ не существует. 
  
Возвращаемое значение является положительным, если точка находится слева от направления командировки; является отрицательным точка находится справа от направления командировок.
  

