---
title: Функция LOCTOPAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Возвращает преобразованную точку в родительских координатах в системе координат назначения.
ms.openlocfilehash: 65a08837d7d026836ebc8d5e35938ea049d005e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439984"
---
# <a name="loctopar-function"></a>Функция LOCTOPAR

Возвращает преобразованную точку в родительских координатах в системе координат назначения.
  
## <a name="syntax"></a>Синтаксис

LOCTOPAR(** *srcPoint* **, ** *srcRef* **, ** *dstRef* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _srcPoint_ <br/> |Обязательный  <br/> |**String** <br/> | Точка в локальных координатах в системе координат источника.  <br/> |
| _srcRef_ <br/> |Обязательный  <br/> |**String** <br/> | Ссылка на ячейку в объекте источника.  <br/> |
| _dstRef_ <br/> |Обязательный  <br/> |**String** <br/> | Ссылка на ячейку в объекте назначения.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Преобразует точку из локальных координат в форме источника в родительские координаты в форме назначения. Вы можете использовать функцию LOCTOPAR для набора родительских координат в ячейках, таких как PinX, PinY, BeginX и BeginY в форме, используя другую точку из другой системы координат. 
  
Эта функция работает даже в том случае, если исходные и назначения фигуры находятся в группах. Он также настраивается для вращения и сальто в промежуточной трансформации. 
  
Координаты источника и назначения должны быть на одной странице. 
  
Если местом назначения является страница, не родительская, результат выражается в локальных координатах страницы. 
  
## <a name="example"></a>Пример

LOCTOPAR(PNT(LocPinX, LocPiny), Ширина, лист.4! Ширина) 
  
Преобразует локальный пин-код фигуры, связанной с формулой, в родительские координаты Sheet.4. 
  

