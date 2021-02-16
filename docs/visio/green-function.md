---
title: Функция GREEN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Возвращает зеленый компонент цвета.
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438108"
---
# <a name="green-function"></a>Функция GREEN

Возвращает зеленый компонент цвета.
  
## <a name="syntax"></a>Синтаксис

GREEN(** *expression* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**Разные** <br/> |Индекс цвета в таблице цветов документа, выражение, которое соеется с пользовательским цветом (например, RGB или HSL) или ссылку на ячейку, которая содержит индекс цвета или результат цвета.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Целое число
  
## <a name="remarks"></a>Замечания

Возвращаемая величина — это число в диапазоне от 0 до 255 включительно или ссылка на ячейку, разрешаемая в индекс. Если  *выражение*  недопустимо, возвращается 0 (черный). 
  
## <a name="example-1"></a>Пример 1

GREEN(Sheet.4! FillForegnd)
  
Возвращает зеленый компонент цвета переднего плана заливки Sheet.4.
  
## <a name="example-2"></a>Пример 2

GREEN(11)
  
Возвращает значение 128, если документ использует цветовую палитру Visio по умолчанию, где темно-желтый цвет — это цвет в индексе 11.
  
## <a name="example-3"></a>Пример 3

GREEN(RGB(10, 20, 30))
  
Возвращает 20.
  

