---
title: Функция HUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Возвращает значение компонента цветового оттенка.
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439494"
---
# <a name="hue-function"></a>Функция HUE

Возвращает значение компонента цветового оттенка.
  
## <a name="syntax"></a>Синтаксис

HUE(** *expression* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательно  <br/> |**Строка** <br/> |Выражение, которое оценивается в цвет.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Числовой
  
## <a name="remarks"></a>Примечания

Возвращаемая величина — это число в диапазоне от 0 до 239 включительно. Входные данные — это индекс цвета в таблице цветов документа, выражение, которое соеется с пользовательским цветом (например, RGB или HSL) или ссылку на ячейку, которая содержит индекс цвета или результат цвета. Функция возвращает 0 для недопустимого ввода. 
  
## <a name="example-1"></a>Пример 1

HUE(Sheet.4! FillForegnd)
  
Возвращает оттенки цвета переднего плана заливки Sheet.4.
  
## <a name="example-2"></a>Пример 2

HUE(7)
  
Возвращает значение 120, если документ использует цветовую палитру Microsoft Visio по умолчанию, где cyan — это цвет в индексе 7.
  
## <a name="example-3"></a>Пример 3

HUE(HSL(10, 20, 30)
  
Возвращает 10.
  

