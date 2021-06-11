---
title: Функция NURBS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Возвращает неоформленную рациональную B-spline (NURBS). Эта функция используется в ячейке E в строках геометрии NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438458"
---
# <a name="nurbs-function"></a>Функция NURBS

Возвращает неоформленную рациональную B-spline (NURBS). Эта функция используется в ячейке E в строках геометрии NURBSTo.
  
## <a name="syntax"></a>Синтаксис

NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Обязательный  <br/> |**строка** <br/> | Последний узел.  <br/> |
| _степень_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Степень spline.  <br/> |
| _xType_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Указывает, как интерпретировать _данные ввода x._ Если  _xType_ — 0, все  _данные ввода x_ интерпретируются как процент ширины. Если  _xType_ — 1, все  _данные ввода x_ интерпретируются как локальные координаты.  <br/> |
| _yType_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Указывает, как интерпретировать _данные ввода y._ Если  _yType_ — 0, все  _данные ввода y_ интерпретируются как процент высоты. Если  _yType_ — 1, все  _данные ввода y_ интерпретируются как локальные координаты.  <br/> |
| _x1_ <br/> |Обязательный  <br/> |**String** <br/> |X-coordinate.  <br/> |
| _y1_ <br/> |Обязательный  <br/> |**String** <br/> |y-coordinate.  <br/> |
| _knot1_ <br/> |Обязательный  <br/> |**String** <br/> |Узел на B-spline.  <br/> |
| _weight1_ <br/> |Обязательный  <br/> |**String** <br/> |Вес на B-spline.  <br/> |
   
## <a name="remarks"></a>Примечания

Для каждого  *аргумента x*  должен быть  *аргумент y;*  в противном случае возвращается ошибка. 
  
Необходимо указать по крайней мере один *аргумент x*, *y*, *узел* и *вес;* в противном Visio возвращает ошибку. 
  

