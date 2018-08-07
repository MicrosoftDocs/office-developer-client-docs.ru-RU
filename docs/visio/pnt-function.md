---
title: Функция PNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Возвращает точки, представленной координаты x и y как одно значение.
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814442"
---
# <a name="pnt-function"></a>Функция PNT

Возвращает точки, представленной координаты _x_ и _y_ как одно значение. 
  
## <a name="syntax"></a>Синтаксис

Раздела PNT (** *x, y* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _x, y_ <br/> |Обязательный  <br/> |**Номер, номер** <br/> |Координаты точки в системе координат текущей фигуры.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Точка
  
## <a name="remarks"></a>Замечания

Преобразование координат в пунктах позволяет изменить Геометрия фигуры без необходимости для работы с *x* - и *y* -координаты отдельно. 
  
## <a name="example"></a>Пример

PNT(PinX,PinY) 
  
Возвращает точки, представленной PinX и PinY. 
  

