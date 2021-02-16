---
title: Функция PAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Возвращает координаты x,y точки в системе координат родительского фигуры.
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414510"
---
# <a name="par-function"></a>Функция PAR

Возвращает  _координаты x,y точки_ в системе координат родительского фигуры. 
  
## <a name="syntax"></a>Синтаксис

PAR(** *point* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |Обязательна  <br/> |**Number, Number** <br/> |Координаты точки в системе координат текущей фигуры.  <br/> |
   
## <a name="remarks"></a>Примечания

В Microsoft Visio точка — это одно значение, которое олицетворяет пару *координат x* и *y.* Если фигура находится в группе, ее родительским является группа. Если фигура не находится в группе, ее родительским сайтом является страница. 
  
## <a name="example"></a>Пример

PAR(PNT(PinX,PinY)) 
  
В этом выражении PNT преобразует пару координат в текущей фигуре в точку. Затем PAR преобразует точку в пару координат относительно левого нижнего угла страницы или группы, содержаной текущую фигуру. 
  

