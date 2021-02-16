---
title: Функция POLYLINE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Возвращает многолинейную линию. Эта функция используется в ячейке A геометрических строк PolyLineTo.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426298"
---
# <a name="polyline-function"></a>Функция POLYLINE

Возвращает многолинейную линию. Эта функция используется в ячейке A геометрических строк PolyLineTo. 
  
## <a name="syntax"></a>Синтаксис

POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Обязательный  <br/> |**Логический** <br/> |Указывает, как интерпретировать _входные данные x._ Если  _xType_ имеет 0, входные  _данные x-data_ интерпретируются как процент ширины. Если  _xType_ имеет 1,  _входные данные x-data_ интерпретируются как локализованная координата.  <br/> |
| _yType_ <br/> |Обязательный  <br/> |**Логический** <br/> |Указывает, как интерпретировать _входные данные y._ Если  _yType_ имеет 0,  _входные данные y_-data интерпретируются как процент высоты. Если  _yType_ имеет 1,  _входные данные y_-data интерпретируются как локализованная координата.  <br/> |
| _x1_ <br/> |Обязательна  <br/> |**Number** <br/> | X-координата.   <br/> |
| _y1_ <br/> |Обязательна  <br/> |**Number** <br/> |Координата _Y._  <br/> |
   
## <a name="remarks"></a>Примечания

Для каждого  *аргумента x*  должен быть аргумент  *y;*  в противном случае возвращается ошибка. 
  
## <a name="example"></a>Пример

POLYLINE (0, 0, 0, 0, 1, 1, 1, 1, 1, 0, 0, 0) 
  
Возвращает прямоугольник размеров Width x Height. 
  

